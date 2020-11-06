---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 0673b0c98e263a0c947fa984267e0eb49ccf9f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519918"
---
# <span data-ttu-id="1b090-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1b090-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="1b090-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b090-102">SYNOPSIS</span></span>
<span data-ttu-id="1b090-103">Crea un criterio di conservazione del backup.</span><span class="sxs-lookup"><span data-stu-id="1b090-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b090-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b090-104">SYNTAX</span></span>

### <span data-ttu-id="1b090-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="1b090-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b090-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="1b090-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b090-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="1b090-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b090-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="1b090-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b090-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="1b090-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b090-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="1b090-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b090-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b090-111">DESCRIPTION</span></span>
<span data-ttu-id="1b090-112">Il cmdlet **New-AzureRmBackupRetentionPolicyObject** crea un criterio di conservazione di Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="1b090-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="1b090-113">I criteri di conservazione definiscono il periodo di tempo in cui il backup mantiene un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1b090-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="1b090-114">I tipi di conservazione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b090-114">The types of retention are the following:</span></span> 

- <span data-ttu-id="1b090-115">Quotidiana</span><span class="sxs-lookup"><span data-stu-id="1b090-115">Daily</span></span> 
- <span data-ttu-id="1b090-116">Settimanale</span><span class="sxs-lookup"><span data-stu-id="1b090-116">Weekly</span></span> 
- <span data-ttu-id="1b090-117">Mensile</span><span class="sxs-lookup"><span data-stu-id="1b090-117">Monthly</span></span> 
- <span data-ttu-id="1b090-118">Annuale</span><span class="sxs-lookup"><span data-stu-id="1b090-118">Yearly</span></span> 

<span data-ttu-id="1b090-119">Creare un criterio di conservazione per ogni tipo di conservazione che si prevede di usare.</span><span class="sxs-lookup"><span data-stu-id="1b090-119">Create one retention policy for each type of retention that you plan to use.</span></span>

<span data-ttu-id="1b090-120">Un criterio di backup è associato ad almeno un criterio di conservazione.</span><span class="sxs-lookup"><span data-stu-id="1b090-120">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="1b090-121">Per creare un criterio di backup, usare il cmdlet New-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b090-121">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="1b090-122">Puoi invece specificare i criteri di conservazione per il cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="1b090-122">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="1b090-123">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b090-123">EXAMPLES</span></span>

### <span data-ttu-id="1b090-124">Esempio 1: creare criteri di conservazione per la conservazione giornaliera</span><span class="sxs-lookup"><span data-stu-id="1b090-124">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="1b090-125">Il primo comando crea un criterio di conservazione per 30 giorni di conservazione giornaliera e lo archivia nella variabile $Daily.</span><span class="sxs-lookup"><span data-stu-id="1b090-125">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="1b090-126">Il secondo comando Visualizza il contenuto di $Daily.</span><span class="sxs-lookup"><span data-stu-id="1b090-126">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="1b090-127">Esempio 2: creare criteri di conservazione mensili</span><span class="sxs-lookup"><span data-stu-id="1b090-127">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="1b090-128">Il primo comando crea un criterio di conservazione che mantiene il backup il decimo e il ventesimo di ogni mese per dodici mesi.</span><span class="sxs-lookup"><span data-stu-id="1b090-128">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="1b090-129">Il comando Archivia i criteri di conservazione nella variabile $Monthly.</span><span class="sxs-lookup"><span data-stu-id="1b090-129">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="1b090-130">Il secondo comando Visualizza il contenuto di $Monthly.</span><span class="sxs-lookup"><span data-stu-id="1b090-130">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="1b090-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b090-131">PARAMETERS</span></span>

### <span data-ttu-id="1b090-132">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="1b090-132">-DailyRetention</span></span>
<span data-ttu-id="1b090-133">Indica che questo cmdlet crea criteri di conservazione giornalieri.</span><span class="sxs-lookup"><span data-stu-id="1b090-133">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-134">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="1b090-134">-DaysOfMonth</span></span>
<span data-ttu-id="1b090-135">Specifica i giorni del mese che identificano il mantenimento del backup dei punti di ripristino e per quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="1b090-135">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="1b090-136">I valori accettabili per questo parametro sono: numeri interi da 1 a 28 e ultimo.</span><span class="sxs-lookup"><span data-stu-id="1b090-136">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="1b090-137">Specificare questo parametro se si specificano i parametri *DailyRetention* , *MonthlyRetentionInDailyFormat* e *YearlyRetentionInDailyFormat* .</span><span class="sxs-lookup"><span data-stu-id="1b090-137">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-138">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="1b090-138">-DaysOfWeek</span></span>
<span data-ttu-id="1b090-139">Specifica una matrice di giorni della settimana.</span><span class="sxs-lookup"><span data-stu-id="1b090-139">Specifies an array of days of the week.</span></span>
<span data-ttu-id="1b090-140">I giorni specificati in questo cmdlet identificano i punti di ripristino che il backup mantiene e per quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="1b090-140">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="1b090-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b090-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b090-142">Lunedì</span><span class="sxs-lookup"><span data-stu-id="1b090-142">Monday</span></span> 
- <span data-ttu-id="1b090-143">Martedì</span><span class="sxs-lookup"><span data-stu-id="1b090-143">Tuesday</span></span> 
- <span data-ttu-id="1b090-144">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="1b090-144">Wednesday</span></span> 
- <span data-ttu-id="1b090-145">Giovedì</span><span class="sxs-lookup"><span data-stu-id="1b090-145">Thursday</span></span> 
- <span data-ttu-id="1b090-146">Venerdì</span><span class="sxs-lookup"><span data-stu-id="1b090-146">Friday</span></span> 
- <span data-ttu-id="1b090-147">Sabato</span><span class="sxs-lookup"><span data-stu-id="1b090-147">Saturday</span></span> 
- <span data-ttu-id="1b090-148">Domenica</span><span class="sxs-lookup"><span data-stu-id="1b090-148">Sunday</span></span>

<span data-ttu-id="1b090-149">Specificare questo parametro se si specificano i parametri *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* e *YearlyRetentionInWeeklyFormat* .</span><span class="sxs-lookup"><span data-stu-id="1b090-149">Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>

<span data-ttu-id="1b090-150">Assicurarsi che i giorni della settimana selezionati per il backup e per la conservazione siano allineati.</span><span class="sxs-lookup"><span data-stu-id="1b090-150">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="1b090-151">Ad esempio, se il backup è impostato per il sabato, i criteri di conservazione devono usare anche sabato.</span><span class="sxs-lookup"><span data-stu-id="1b090-151">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b090-152">-DefaultProfile</span></span>
<span data-ttu-id="1b090-153">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1b090-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-154">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="1b090-154">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="1b090-155">Indica che questo cmdlet crea un criterio mensile in formato giornaliero.</span><span class="sxs-lookup"><span data-stu-id="1b090-155">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-156">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="1b090-156">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="1b090-157">Indica che questo cmdlet crea un criterio mensile in formato settimanale.</span><span class="sxs-lookup"><span data-stu-id="1b090-157">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-158">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="1b090-158">-MonthsOfYear</span></span>
<span data-ttu-id="1b090-159">Specifica i mesi dell'anno con i punti di ripristino che il backup mantiene annualmente.</span><span class="sxs-lookup"><span data-stu-id="1b090-159">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="1b090-160">I valori accettabili per questo parametro sono: nomi di mesi, ad esempio gennaio o febbraio.</span><span class="sxs-lookup"><span data-stu-id="1b090-160">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-161">-Conservazione</span><span class="sxs-lookup"><span data-stu-id="1b090-161">-Retention</span></span>
<span data-ttu-id="1b090-162">Specifica il periodo di conservazione, in giorni, mesi o anni, per cui il backup archivia un punto di backup.</span><span class="sxs-lookup"><span data-stu-id="1b090-162">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="1b090-163">L'unità dipende dal fatto che questo cmdlet selezioni un'opzione di conservazione giornaliera, mensile o annuale.</span><span class="sxs-lookup"><span data-stu-id="1b090-163">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="1b090-164">Se ad esempio specifichi il parametro *DailyRetention* , il cmdlet interpreta il parametro Current come numero di giorni.</span><span class="sxs-lookup"><span data-stu-id="1b090-164">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-165">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="1b090-165">-WeeklyRetention</span></span>
<span data-ttu-id="1b090-166">Indica che questo cmdlet crea criteri di conservazione settimanali.</span><span class="sxs-lookup"><span data-stu-id="1b090-166">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-167">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="1b090-167">-WeekNumber</span></span>
<span data-ttu-id="1b090-168">Specifica le settimane del mese che identificano il mantenimento dei punti di ripristino e per quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="1b090-168">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="1b090-169">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b090-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b090-170">Prima</span><span class="sxs-lookup"><span data-stu-id="1b090-170">First</span></span> 
- <span data-ttu-id="1b090-171">Secondo</span><span class="sxs-lookup"><span data-stu-id="1b090-171">Second</span></span> 
- <span data-ttu-id="1b090-172">Terze</span><span class="sxs-lookup"><span data-stu-id="1b090-172">Third</span></span> 
- <span data-ttu-id="1b090-173">Quarto</span><span class="sxs-lookup"><span data-stu-id="1b090-173">Fourth</span></span> 
- <span data-ttu-id="1b090-174">Ultima</span><span class="sxs-lookup"><span data-stu-id="1b090-174">Last</span></span>

```yaml
Type: String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-175">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="1b090-175">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="1b090-176">Indica che questo cmdlet crea un criterio di conservazione annuale nel formato giornaliero.</span><span class="sxs-lookup"><span data-stu-id="1b090-176">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-177">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="1b090-177">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="1b090-178">Indica che questo cmdlet crea un criterio di conservazione annuale in formato settimanale.</span><span class="sxs-lookup"><span data-stu-id="1b090-178">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b090-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b090-179">CommonParameters</span></span>
<span data-ttu-id="1b090-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b090-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b090-181">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b090-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b090-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b090-182">INPUTS</span></span>

### <span data-ttu-id="1b090-183">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b090-183">None</span></span>

## <span data-ttu-id="1b090-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b090-184">OUTPUTS</span></span>

### <span data-ttu-id="1b090-185">AzureRmBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b090-185">AzureRmBackupRetentionPolicy</span></span>

## <span data-ttu-id="1b090-186">Note</span><span class="sxs-lookup"><span data-stu-id="1b090-186">NOTES</span></span>
* <span data-ttu-id="1b090-187">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b090-187">None</span></span>

## <span data-ttu-id="1b090-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b090-188">RELATED LINKS</span></span>

[<span data-ttu-id="1b090-189">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1b090-189">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="1b090-190">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b090-190">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


