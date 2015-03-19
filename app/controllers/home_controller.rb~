class HomeController < ApplicationController
  
  #controller method which accepts the parameters and processes to generate the output
  def index
    if params[:n_value].present? && params[:k_value].present?
      #parsing the parameters and casting them to integer
      n = params[:n_value].to_i
      k = params[:k_value].to_i
      total = 0
      @result = []    #resultset object which is used to display the output
      if(n>0 )
        if(k>0 && k<=n)
          for i in 1..(n-2)
            for j in i..(n-1-i)
              k= n-i-j
              if(k>=j)
                total = total+1
                @result << "#{i} + #{j} + #{k} = #{n}"      #the unique equation strings to be displayed are pushed to the resultset object
              end
            end
          end
        end
      end
    else
      @result = nil     #if the resultset is nil
    end
  end
end
