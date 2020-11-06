---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 740077def0ba0eccb1d962b88317fadb3c5c897c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509359"
---
# <span data-ttu-id="da68f-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="da68f-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="da68f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da68f-102">SYNOPSIS</span></span>
<span data-ttu-id="da68f-103">Crea un criterio di conservazione del backup.</span><span class="sxs-lookup"><span data-stu-id="da68f-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da68f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da68f-104">SYNTAX</span></span>

### <span data-ttu-id="da68f-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="da68f-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da68f-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="da68f-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da68f-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="da68f-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da68f-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="da68f-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da68f-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="da68f-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da68f-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="da68f-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da68f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da68f-111">DESCRIPTION</span></span>
<span data-ttu-id="da68f-112">Il cmdlet **New-AzureRmBackupRetentionPolicyObject** crea un criterio di conservazione di Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="da68f-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="da68f-113">I criteri di conservazione definiscono il periodo di tempo in cui il backup mantiene un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="da68f-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="da68f-114">I tipi di conservazione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="da68f-114">The types of retention are the following:</span></span> 
- <span data-ttu-id="da68f-115">Quotidiana</span><span class="sxs-lookup"><span data-stu-id="da68f-115">Daily</span></span> 
- <span data-ttu-id="da68f-116">Settimanale</span><span class="sxs-lookup"><span data-stu-id="da68f-116">Weekly</span></span> 
- <span data-ttu-id="da68f-117">Mensile</span><span class="sxs-lookup"><span data-stu-id="da68f-117">Monthly</span></span> 
- <span data-ttu-id="da68f-118">Creare annualmente uno dei criteri di conservazione per ogni tipo di conservazione che si prevede di usare.</span><span class="sxs-lookup"><span data-stu-id="da68f-118">Yearly Create one retention policy for each type of retention that you plan to use.</span></span>
<span data-ttu-id="da68f-119">Un criterio di backup è associato ad almeno un criterio di conservazione.</span><span class="sxs-lookup"><span data-stu-id="da68f-119">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="da68f-120">Per creare un criterio di backup, usare il cmdlet New-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="da68f-120">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="da68f-121">Puoi invece specificare i criteri di conservazione per il cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="da68f-121">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="da68f-122">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da68f-122">EXAMPLES</span></span>

### <span data-ttu-id="da68f-123">Esempio 1: creare criteri di conservazione per la conservazione giornaliera</span><span class="sxs-lookup"><span data-stu-id="da68f-123">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="da68f-124">Il primo comando crea un criterio di conservazione per 30 giorni di conservazione giornaliera e lo archivia nella variabile $Daily.</span><span class="sxs-lookup"><span data-stu-id="da68f-124">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="da68f-125">Il secondo comando Visualizza il contenuto di $Daily.</span><span class="sxs-lookup"><span data-stu-id="da68f-125">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="da68f-126">Esempio 2: creare criteri di conservazione mensili</span><span class="sxs-lookup"><span data-stu-id="da68f-126">Example 2: Create a monthly retention policy</span></span>
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

<span data-ttu-id="da68f-127">Il primo comando crea un criterio di conservazione che mantiene il backup il decimo e il ventesimo di ogni mese per dodici mesi.</span><span class="sxs-lookup"><span data-stu-id="da68f-127">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="da68f-128">Il comando Archivia i criteri di conservazione nella variabile $Monthly.</span><span class="sxs-lookup"><span data-stu-id="da68f-128">The command stores the retention policy in the $Monthly variable.</span></span>
<span data-ttu-id="da68f-129">Il secondo comando Visualizza il contenuto di $Monthly.</span><span class="sxs-lookup"><span data-stu-id="da68f-129">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="da68f-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da68f-130">PARAMETERS</span></span>

### <span data-ttu-id="da68f-131">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="da68f-131">-DailyRetention</span></span>
<span data-ttu-id="da68f-132">Indica che questo cmdlet crea criteri di conservazione giornalieri.</span><span class="sxs-lookup"><span data-stu-id="da68f-132">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-133">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="da68f-133">-DaysOfMonth</span></span>
<span data-ttu-id="da68f-134">Specifica i giorni del mese che identificano il mantenimento del backup dei punti di ripristino e per quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="da68f-134">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="da68f-135">I valori accettabili per questo parametro sono: numeri interi da 1 a 28 e ultimo.</span><span class="sxs-lookup"><span data-stu-id="da68f-135">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="da68f-136">Specificare questo parametro se si specificano i parametri *DailyRetention* , *MonthlyRetentionInDailyFormat* e *YearlyRetentionInDailyFormat* .</span><span class="sxs-lookup"><span data-stu-id="da68f-136">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

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

### <span data-ttu-id="da68f-137">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="da68f-137">-DaysOfWeek</span></span>
<span data-ttu-id="da68f-138">Specifica una matrice di giorni della settimana.</span><span class="sxs-lookup"><span data-stu-id="da68f-138">Specifies an array of days of the week.</span></span>
<span data-ttu-id="da68f-139">I giorni specificati in questo cmdlet identificano i punti di ripristino che il backup mantiene e per quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="da68f-139">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="da68f-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="da68f-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da68f-141">Lunedì</span><span class="sxs-lookup"><span data-stu-id="da68f-141">Monday</span></span> 
- <span data-ttu-id="da68f-142">Martedì</span><span class="sxs-lookup"><span data-stu-id="da68f-142">Tuesday</span></span> 
- <span data-ttu-id="da68f-143">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="da68f-143">Wednesday</span></span> 
- <span data-ttu-id="da68f-144">Giovedì</span><span class="sxs-lookup"><span data-stu-id="da68f-144">Thursday</span></span> 
- <span data-ttu-id="da68f-145">Venerdì</span><span class="sxs-lookup"><span data-stu-id="da68f-145">Friday</span></span> 
- <span data-ttu-id="da68f-146">Sabato</span><span class="sxs-lookup"><span data-stu-id="da68f-146">Saturday</span></span> 
- <span data-ttu-id="da68f-147">Domenica specificare questo parametro se si specificano i parametri *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* e *YearlyRetentionInWeeklyFormat* .</span><span class="sxs-lookup"><span data-stu-id="da68f-147">Sunday Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>
<span data-ttu-id="da68f-148">Assicurarsi che i giorni della settimana selezionati per il backup e per la conservazione siano allineati.</span><span class="sxs-lookup"><span data-stu-id="da68f-148">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="da68f-149">Ad esempio, se il backup è impostato per il sabato, i criteri di conservazione devono usare anche sabato.</span><span class="sxs-lookup"><span data-stu-id="da68f-149">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da68f-150">-DefaultProfile</span></span>
<span data-ttu-id="da68f-151">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="da68f-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="da68f-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="da68f-153">Indica che questo cmdlet crea un criterio mensile in formato giornaliero.</span><span class="sxs-lookup"><span data-stu-id="da68f-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="da68f-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="da68f-155">Indica che questo cmdlet crea un criterio mensile in formato settimanale.</span><span class="sxs-lookup"><span data-stu-id="da68f-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="da68f-156">-MonthsOfYear</span></span>
<span data-ttu-id="da68f-157">Specifica i mesi dell'anno con i punti di ripristino che il backup mantiene annualmente.</span><span class="sxs-lookup"><span data-stu-id="da68f-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="da68f-158">I valori accettabili per questo parametro sono: nomi di mesi, ad esempio gennaio o febbraio.</span><span class="sxs-lookup"><span data-stu-id="da68f-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-159">-Conservazione</span><span class="sxs-lookup"><span data-stu-id="da68f-159">-Retention</span></span>
<span data-ttu-id="da68f-160">Specifica il periodo di conservazione, in giorni, mesi o anni, per cui il backup archivia un punto di backup.</span><span class="sxs-lookup"><span data-stu-id="da68f-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="da68f-161">L'unità dipende dal fatto che questo cmdlet selezioni un'opzione di conservazione giornaliera, mensile o annuale.</span><span class="sxs-lookup"><span data-stu-id="da68f-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="da68f-162">Se ad esempio specifichi il parametro *DailyRetention* , il cmdlet interpreta il parametro Current come numero di giorni.</span><span class="sxs-lookup"><span data-stu-id="da68f-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="da68f-163">-WeeklyRetention</span></span>
<span data-ttu-id="da68f-164">Indica che questo cmdlet crea criteri di conservazione settimanali.</span><span class="sxs-lookup"><span data-stu-id="da68f-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="da68f-165">-WeekNumber</span></span>
<span data-ttu-id="da68f-166">Specifica le settimane del mese che identificano il mantenimento dei punti di ripristino e per quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="da68f-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="da68f-167">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="da68f-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da68f-168">Prima</span><span class="sxs-lookup"><span data-stu-id="da68f-168">First</span></span> 
- <span data-ttu-id="da68f-169">Secondo</span><span class="sxs-lookup"><span data-stu-id="da68f-169">Second</span></span> 
- <span data-ttu-id="da68f-170">Terze</span><span class="sxs-lookup"><span data-stu-id="da68f-170">Third</span></span> 
- <span data-ttu-id="da68f-171">Quarto</span><span class="sxs-lookup"><span data-stu-id="da68f-171">Fourth</span></span> 
- <span data-ttu-id="da68f-172">Ultima</span><span class="sxs-lookup"><span data-stu-id="da68f-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="da68f-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="da68f-174">Indica che questo cmdlet crea un criterio di conservazione annuale nel formato giornaliero.</span><span class="sxs-lookup"><span data-stu-id="da68f-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="da68f-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="da68f-176">Indica che questo cmdlet crea un criterio di conservazione annuale in formato settimanale.</span><span class="sxs-lookup"><span data-stu-id="da68f-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da68f-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da68f-177">CommonParameters</span></span>
<span data-ttu-id="da68f-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da68f-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da68f-179">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da68f-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da68f-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da68f-180">INPUTS</span></span>

### <span data-ttu-id="da68f-181">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da68f-181">None</span></span>

## <span data-ttu-id="da68f-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da68f-182">OUTPUTS</span></span>

### <span data-ttu-id="da68f-183">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="da68f-183">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy</span></span>

## <span data-ttu-id="da68f-184">Note</span><span class="sxs-lookup"><span data-stu-id="da68f-184">NOTES</span></span>
* <span data-ttu-id="da68f-185">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da68f-185">None</span></span>

## <span data-ttu-id="da68f-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da68f-186">RELATED LINKS</span></span>

[<span data-ttu-id="da68f-187">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="da68f-187">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="da68f-188">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="da68f-188">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


