---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cf099afe95eec37e070cc2b09d30b7f4b2766b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968078"
---
# <span data-ttu-id="2e642-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="2e642-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="2e642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e642-102">SYNOPSIS</span></span>
<span data-ttu-id="2e642-103">Aggiorna un criterio di snapshot dei file ANF di Azure ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="2e642-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="2e642-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e642-104">SYNTAX</span></span>

### <span data-ttu-id="2e642-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e642-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e642-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e642-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e642-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e642-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e642-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e642-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e642-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e642-109">DESCRIPTION</span></span>
<span data-ttu-id="2e642-110">Il cmdlet **Update-AzNetAppFilesSnapshotPolicy** modifica un criterio snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="2e642-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="2e642-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e642-111">EXAMPLES</span></span>

### <span data-ttu-id="2e642-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e642-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="2e642-113">Questo comando modifica il criterio di backup ANF "MySnapshotPolicy" in modo da impostare il programma orario specificato.</span><span class="sxs-lookup"><span data-stu-id="2e642-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="2e642-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e642-114">PARAMETERS</span></span>

### <span data-ttu-id="2e642-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e642-115">-AccountName</span></span>
<span data-ttu-id="2e642-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="2e642-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="2e642-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="2e642-117">-AccountObject</span></span>
<span data-ttu-id="2e642-118">Account per il nuovo oggetto Criterio snapshot</span><span class="sxs-lookup"><span data-stu-id="2e642-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="2e642-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="2e642-119">-DailySchedule</span></span>
<span data-ttu-id="2e642-120">Matrice di tabella hash che rappresenta la pianificazione giornaliera</span><span class="sxs-lookup"><span data-stu-id="2e642-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e642-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e642-121">-DefaultProfile</span></span>
<span data-ttu-id="2e642-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e642-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e642-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="2e642-123">-Enabled</span></span>
<span data-ttu-id="2e642-124">La proprietà per decidere i criteri è abilitata o meno</span><span class="sxs-lookup"><span data-stu-id="2e642-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e642-125">-Pianificazione oraria</span><span class="sxs-lookup"><span data-stu-id="2e642-125">-HourlySchedule</span></span>
<span data-ttu-id="2e642-126">Matrice di tabella hash che rappresenta la pianificazione oraria</span><span class="sxs-lookup"><span data-stu-id="2e642-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e642-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e642-127">-InputObject</span></span>
<span data-ttu-id="2e642-128">Oggetto snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="2e642-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e642-129">-Location</span><span class="sxs-lookup"><span data-stu-id="2e642-129">-Location</span></span>
<span data-ttu-id="2e642-130">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="2e642-130">The location of the resource</span></span>

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

### <span data-ttu-id="2e642-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="2e642-131">-MonthlySchedule</span></span>
<span data-ttu-id="2e642-132">Matrice di tabella hash che rappresenta la funzione Pianificazione montly</span><span class="sxs-lookup"><span data-stu-id="2e642-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e642-133">-Name</span><span class="sxs-lookup"><span data-stu-id="2e642-133">-Name</span></span>
<span data-ttu-id="2e642-134">Nome dei criteri snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="2e642-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e642-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e642-135">-ResourceGroupName</span></span>
<span data-ttu-id="2e642-136">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="2e642-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2e642-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e642-137">-ResourceId</span></span>
<span data-ttu-id="2e642-138">ID risorsa dei criteri snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="2e642-138">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e642-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e642-139">-Tag</span></span>
<span data-ttu-id="2e642-140">Matrice di tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="2e642-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="2e642-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="2e642-141">-WeeklySchedule</span></span>
<span data-ttu-id="2e642-142">Matrice di tabella hash che rappresenta la funzione Pianificazione montly</span><span class="sxs-lookup"><span data-stu-id="2e642-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e642-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e642-143">-Confirm</span></span>
<span data-ttu-id="2e642-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e642-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e642-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e642-145">-WhatIf</span></span>
<span data-ttu-id="2e642-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e642-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e642-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e642-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e642-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e642-148">CommonParameters</span></span>
<span data-ttu-id="2e642-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e642-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e642-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e642-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e642-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e642-151">INPUTS</span></span>

### <span data-ttu-id="2e642-152">System.String</span><span class="sxs-lookup"><span data-stu-id="2e642-152">System.String</span></span>

### <span data-ttu-id="2e642-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2e642-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="2e642-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="2e642-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="2e642-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e642-155">OUTPUTS</span></span>

### <span data-ttu-id="2e642-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="2e642-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="2e642-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e642-157">NOTES</span></span>

## <span data-ttu-id="2e642-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e642-158">RELATED LINKS</span></span>
