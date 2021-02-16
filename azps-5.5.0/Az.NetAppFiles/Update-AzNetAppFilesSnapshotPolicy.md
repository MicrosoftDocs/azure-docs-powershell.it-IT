---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194023"
---
# <span data-ttu-id="9a1f7-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="9a1f7-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="9a1f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1f7-103">Aggiorna un criterio di snapshot dei file ANF di Azure ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="9a1f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a1f7-104">SYNTAX</span></span>

### <span data-ttu-id="9a1f7-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a1f7-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1f7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1f7-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1f7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1f7-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1f7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1f7-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a1f7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9a1f7-109">DESCRIPTION</span></span>
<span data-ttu-id="9a1f7-110">Il cmdlet **Update-AzNetAppFilesSnapshotPolicy** modifica un criterio snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="9a1f7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a1f7-111">EXAMPLES</span></span>

### <span data-ttu-id="9a1f7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a1f7-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="9a1f7-113">Questo comando modifica il criterio di backup ANF "MySnapshotPolicy" in modo da impostare il programma orario specificato.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="9a1f7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a1f7-114">PARAMETERS</span></span>

### <span data-ttu-id="9a1f7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9a1f7-115">-AccountName</span></span>
<span data-ttu-id="9a1f7-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="9a1f7-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9a1f7-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="9a1f7-117">-AccountObject</span></span>
<span data-ttu-id="9a1f7-118">Account per il nuovo oggetto Criterio snapshot</span><span class="sxs-lookup"><span data-stu-id="9a1f7-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="9a1f7-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="9a1f7-119">-DailySchedule</span></span>
<span data-ttu-id="9a1f7-120">Matrice di tabella hash che rappresenta la pianificazione giornaliera</span><span class="sxs-lookup"><span data-stu-id="9a1f7-120">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="9a1f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a1f7-121">-DefaultProfile</span></span>
<span data-ttu-id="9a1f7-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a1f7-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9a1f7-123">-Enabled</span></span>
<span data-ttu-id="9a1f7-124">La proprietà per decidere i criteri è abilitata o meno</span><span class="sxs-lookup"><span data-stu-id="9a1f7-124">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="9a1f7-125">-Pianificazione oraria</span><span class="sxs-lookup"><span data-stu-id="9a1f7-125">-HourlySchedule</span></span>
<span data-ttu-id="9a1f7-126">Matrice di tabella hash che rappresenta la pianificazione oraria</span><span class="sxs-lookup"><span data-stu-id="9a1f7-126">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="9a1f7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a1f7-127">-InputObject</span></span>
<span data-ttu-id="9a1f7-128">Oggetto snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="9a1f7-128">The snapshot object to remove</span></span>

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

### <span data-ttu-id="9a1f7-129">-Location</span><span class="sxs-lookup"><span data-stu-id="9a1f7-129">-Location</span></span>
<span data-ttu-id="9a1f7-130">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="9a1f7-130">The location of the resource</span></span>

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

### <span data-ttu-id="9a1f7-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="9a1f7-131">-MonthlySchedule</span></span>
<span data-ttu-id="9a1f7-132">Matrice di tabella hash che rappresenta la funzione Pianificazione montly</span><span class="sxs-lookup"><span data-stu-id="9a1f7-132">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="9a1f7-133">-Name</span><span class="sxs-lookup"><span data-stu-id="9a1f7-133">-Name</span></span>
<span data-ttu-id="9a1f7-134">Nome dei criteri snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="9a1f7-134">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="9a1f7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a1f7-135">-ResourceGroupName</span></span>
<span data-ttu-id="9a1f7-136">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="9a1f7-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9a1f7-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a1f7-137">-ResourceId</span></span>
<span data-ttu-id="9a1f7-138">ID risorsa dei criteri snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="9a1f7-138">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="9a1f7-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="9a1f7-139">-Tag</span></span>
<span data-ttu-id="9a1f7-140">Matrice di tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="9a1f7-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="9a1f7-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="9a1f7-141">-WeeklySchedule</span></span>
<span data-ttu-id="9a1f7-142">Matrice di tabella hash che rappresenta la funzione Pianificazione montly</span><span class="sxs-lookup"><span data-stu-id="9a1f7-142">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="9a1f7-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a1f7-143">-Confirm</span></span>
<span data-ttu-id="9a1f7-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a1f7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a1f7-145">-WhatIf</span></span>
<span data-ttu-id="9a1f7-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a1f7-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a1f7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1f7-148">CommonParameters</span></span>
<span data-ttu-id="9a1f7-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1f7-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9a1f7-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1f7-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="9a1f7-151">INPUTS</span></span>

### <span data-ttu-id="9a1f7-152">System.String</span><span class="sxs-lookup"><span data-stu-id="9a1f7-152">System.String</span></span>

### <span data-ttu-id="9a1f7-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9a1f7-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="9a1f7-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="9a1f7-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="9a1f7-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a1f7-155">OUTPUTS</span></span>

### <span data-ttu-id="9a1f7-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="9a1f7-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="9a1f7-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="9a1f7-157">NOTES</span></span>

## <span data-ttu-id="9a1f7-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a1f7-158">RELATED LINKS</span></span>
