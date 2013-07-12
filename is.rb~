class SpiralMatrix
  def initialize(n)
    @n = n.to_i
    @side = Math.sqrt(@n).to_i
    raise Exception, "Please enter perfect square number" if @side*@side != @n or @n == 0
    @digits = @n.to_s.length+1
    @matrix = Hash.new{|h,k| h[k]=[]}
    fill_matrix
  end

  def fill_matrix
    z = @n
    offset_row = offset_col = 0
    max_row = max_col = @side - 1
    while offset_row <= max_row && offset_col <= max_col do
      for i in offset_col..max_col
        @matrix[offset_row][i] = z
        z -= 1
      end
      offset_row += 1

      for i in offset_row..max_row
        @matrix[i][max_col] = z
        z -= 1
      end
      max_col -= 1

      if offset_row < max_row
        for i in max_col.downto(offset_col)
          @matrix[max_row][i] = z
          z -= 1
        end
        max_row -= 1
      end

      if offset_col < max_col
        for i in max_row.downto(offset_row)
          @matrix[i][offset_col] = z
          z -= 1
        end
        offset_col += 1
      end
    end
  end

  def output
    output_string ||= "Output:"
    @side.times do |row|
      @side.times do |col|
        output_string << "%#{@digits}d" % @matrix[row][col]
      end
      output_string << "\n       "
    end
		output_string << "\n"
		return output_string if output_string.length > 0
  end

end
# is check arguments is number and convert
def safe_parse(satin)
  if satin =~ /\A\d+\Z/
    satin.to_i
  else
    raise Exception
  end
end

ARGV.each do |ar|
  begin
    safe_parse(ar)
    spiral_matrix = SpiralMatrix.new(ar)
    puts "Input:  #{ar}"
    print spiral_matrix.output
  rescue Exception
    puts "Input:  #{ar} is invalid, Please enter perfect square number"
  end
end
puts "Work done!"	   













