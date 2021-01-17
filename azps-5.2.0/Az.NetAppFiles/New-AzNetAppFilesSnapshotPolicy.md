---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359908"
---
# <span data-ttu-id="2a25b-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="2a25b-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="2a25b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a25b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a25b-103">Crea un nuovo criterio di snapshot di Azure NetApp Files (ANF) per un account ANF.</span><span class="sxs-lookup"><span data-stu-id="2a25b-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="2a25b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a25b-104">SYNTAX</span></span>

### <span data-ttu-id="2a25b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a25b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a25b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a25b-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a25b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a25b-107">DESCRIPTION</span></span>
<span data-ttu-id="2a25b-108">Il cmdlet **New-AzNetAppFilesActiveDirectory** crea un nuovo criterio snapshot per un account ANF.</span><span class="sxs-lookup"><span data-stu-id="2a25b-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="2a25b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a25b-109">EXAMPLES</span></span>

### <span data-ttu-id="2a25b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2a25b-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="2a25b-111">Questo comando crea i nuovi criteri di snapshot di ANF per l'account ANF denominato account "account".</span><span class="sxs-lookup"><span data-stu-id="2a25b-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="2a25b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a25b-112">PARAMETERS</span></span>

### <span data-ttu-id="2a25b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2a25b-113">-AccountName</span></span>
<span data-ttu-id="2a25b-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="2a25b-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="2a25b-115">-AccountObject</span></span>
<span data-ttu-id="2a25b-116">Account per il nuovo oggetto Criteri snapshot</span><span class="sxs-lookup"><span data-stu-id="2a25b-116">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="2a25b-117">-DailySchedule</span></span>
<span data-ttu-id="2a25b-118">Matrice Hashtable che rappresenta la programmazione giornaliera</span><span class="sxs-lookup"><span data-stu-id="2a25b-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a25b-119">-DefaultProfile</span></span>
<span data-ttu-id="2a25b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a25b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="2a25b-121">-Enabled</span></span>
<span data-ttu-id="2a25b-122">La proprietà per decidere i criteri è abilitata o meno</span><span class="sxs-lookup"><span data-stu-id="2a25b-122">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="2a25b-123">-HourlySchedule</span></span>
<span data-ttu-id="2a25b-124">Matrice Hashtable che rappresenta la programmazione oraria</span><span class="sxs-lookup"><span data-stu-id="2a25b-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2a25b-125">-Location</span></span>
<span data-ttu-id="2a25b-126">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="2a25b-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="2a25b-127">-MonthlySchedule</span></span>
<span data-ttu-id="2a25b-128">Matrice Hashtable che rappresenta la pianificazione mensile</span><span class="sxs-lookup"><span data-stu-id="2a25b-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a25b-129">-Name</span></span>
<span data-ttu-id="2a25b-130">Nome dei criteri di snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="2a25b-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a25b-131">-ResourceGroupName</span></span>
<span data-ttu-id="2a25b-132">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="2a25b-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a25b-133">-Tag</span></span>
<span data-ttu-id="2a25b-134">Matrice Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="2a25b-134">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="2a25b-135">-WeeklySchedule</span></span>
<span data-ttu-id="2a25b-136">Matrice Hashtable che rappresenta la pianificazione mensile</span><span class="sxs-lookup"><span data-stu-id="2a25b-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a25b-137">-Confirm</span></span>
<span data-ttu-id="2a25b-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a25b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a25b-139">-WhatIf</span></span>
<span data-ttu-id="2a25b-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a25b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a25b-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a25b-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a25b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a25b-142">CommonParameters</span></span>
<span data-ttu-id="2a25b-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a25b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a25b-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a25b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a25b-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a25b-145">INPUTS</span></span>

### <span data-ttu-id="2a25b-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2a25b-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2a25b-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a25b-147">OUTPUTS</span></span>

### <span data-ttu-id="2a25b-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="2a25b-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="2a25b-149">Note</span><span class="sxs-lookup"><span data-stu-id="2a25b-149">NOTES</span></span>

## <span data-ttu-id="2a25b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a25b-150">RELATED LINKS</span></span>
