---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192071"
---
# <span data-ttu-id="1cb1c-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1cb1c-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1cb1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb1c-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb1c-103">Crea un nuovo criterio snapshot per i file ANF di Azure NetApp per un account ANF.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="1cb1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cb1c-104">SYNTAX</span></span>

### <span data-ttu-id="1cb1c-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1cb1c-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb1c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb1c-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb1c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1cb1c-107">DESCRIPTION</span></span>
<span data-ttu-id="1cb1c-108">Il cmdlet **New-AzNetAppFilesActiveDirectory** crea un nuovo criterio snapshot per un account ANF.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="1cb1c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cb1c-109">EXAMPLES</span></span>

### <span data-ttu-id="1cb1c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1cb1c-110">Example 1</span></span>
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

<span data-ttu-id="1cb1c-111">Questo comando crea il nuovo criterio snapshot ANF per l'account ANF denominato account "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="1cb1c-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="1cb1c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cb1c-112">PARAMETERS</span></span>

### <span data-ttu-id="1cb1c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1cb1c-113">-AccountName</span></span>
<span data-ttu-id="1cb1c-114">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="1cb1c-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="1cb1c-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1cb1c-115">-AccountObject</span></span>
<span data-ttu-id="1cb1c-116">Account per il nuovo oggetto Criterio snapshot</span><span class="sxs-lookup"><span data-stu-id="1cb1c-116">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="1cb1c-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="1cb1c-117">-DailySchedule</span></span>
<span data-ttu-id="1cb1c-118">Matrice di tabella hash che rappresenta la pianificazione giornaliera</span><span class="sxs-lookup"><span data-stu-id="1cb1c-118">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="1cb1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb1c-119">-DefaultProfile</span></span>
<span data-ttu-id="1cb1c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cb1c-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="1cb1c-121">-Enabled</span></span>
<span data-ttu-id="1cb1c-122">La proprietà per decidere i criteri è abilitata o meno</span><span class="sxs-lookup"><span data-stu-id="1cb1c-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="1cb1c-123">-Pianificazione oraria</span><span class="sxs-lookup"><span data-stu-id="1cb1c-123">-HourlySchedule</span></span>
<span data-ttu-id="1cb1c-124">Matrice di tabella hash che rappresenta la pianificazione oraria</span><span class="sxs-lookup"><span data-stu-id="1cb1c-124">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="1cb1c-125">-Location</span><span class="sxs-lookup"><span data-stu-id="1cb1c-125">-Location</span></span>
<span data-ttu-id="1cb1c-126">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="1cb1c-126">The location of the resource</span></span>

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

### <span data-ttu-id="1cb1c-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="1cb1c-127">-MonthlySchedule</span></span>
<span data-ttu-id="1cb1c-128">Matrice di tabella hash che rappresenta la funzione Pianificazione montly</span><span class="sxs-lookup"><span data-stu-id="1cb1c-128">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="1cb1c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1cb1c-129">-Name</span></span>
<span data-ttu-id="1cb1c-130">Nome dei criteri snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="1cb1c-130">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="1cb1c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb1c-131">-ResourceGroupName</span></span>
<span data-ttu-id="1cb1c-132">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="1cb1c-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1cb1c-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="1cb1c-133">-Tag</span></span>
<span data-ttu-id="1cb1c-134">Matrice di tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="1cb1c-134">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="1cb1c-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="1cb1c-135">-WeeklySchedule</span></span>
<span data-ttu-id="1cb1c-136">Matrice di tabella hash che rappresenta la funzione Pianificazione montly</span><span class="sxs-lookup"><span data-stu-id="1cb1c-136">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="1cb1c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb1c-137">-Confirm</span></span>
<span data-ttu-id="1cb1c-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb1c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb1c-139">-WhatIf</span></span>
<span data-ttu-id="1cb1c-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb1c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb1c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb1c-142">CommonParameters</span></span>
<span data-ttu-id="1cb1c-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb1c-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb1c-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="1cb1c-145">INPUTS</span></span>

### <span data-ttu-id="1cb1c-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1cb1c-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1cb1c-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cb1c-147">OUTPUTS</span></span>

### <span data-ttu-id="1cb1c-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1cb1c-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1cb1c-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="1cb1c-149">NOTES</span></span>

## <span data-ttu-id="1cb1c-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cb1c-150">RELATED LINKS</span></span>
