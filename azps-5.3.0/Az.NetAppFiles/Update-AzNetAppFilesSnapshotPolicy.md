---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380432"
---
# <span data-ttu-id="1c757-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1c757-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1c757-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c757-102">SYNOPSIS</span></span>
<span data-ttu-id="1c757-103">Aggiorna i criteri di snapshot di Azure NetApp (ANF) ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="1c757-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="1c757-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c757-104">SYNTAX</span></span>

### <span data-ttu-id="1c757-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c757-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c757-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c757-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c757-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c757-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c757-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c757-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c757-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c757-109">DESCRIPTION</span></span>
<span data-ttu-id="1c757-110">Il cmdlet **Update-AzNetAppFilesSnapshotPolicy** modifica un criterio di snapshot di ANF.</span><span class="sxs-lookup"><span data-stu-id="1c757-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="1c757-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c757-111">EXAMPLES</span></span>

### <span data-ttu-id="1c757-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c757-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="1c757-113">Questo comando modifica il criterio di backup di ANF "MySnapshotPolicy" per avere l'HourlySchedule specificata.</span><span class="sxs-lookup"><span data-stu-id="1c757-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="1c757-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c757-114">PARAMETERS</span></span>

### <span data-ttu-id="1c757-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1c757-115">-AccountName</span></span>
<span data-ttu-id="1c757-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="1c757-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="1c757-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1c757-117">-AccountObject</span></span>
<span data-ttu-id="1c757-118">Account per il nuovo oggetto Criteri snapshot</span><span class="sxs-lookup"><span data-stu-id="1c757-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="1c757-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="1c757-119">-DailySchedule</span></span>
<span data-ttu-id="1c757-120">Matrice Hashtable che rappresenta la programmazione giornaliera</span><span class="sxs-lookup"><span data-stu-id="1c757-120">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="1c757-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c757-121">-DefaultProfile</span></span>
<span data-ttu-id="1c757-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c757-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c757-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="1c757-123">-Enabled</span></span>
<span data-ttu-id="1c757-124">La proprietà per decidere i criteri è abilitata o meno</span><span class="sxs-lookup"><span data-stu-id="1c757-124">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="1c757-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="1c757-125">-HourlySchedule</span></span>
<span data-ttu-id="1c757-126">Matrice Hashtable che rappresenta la programmazione oraria</span><span class="sxs-lookup"><span data-stu-id="1c757-126">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="1c757-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c757-127">-InputObject</span></span>
<span data-ttu-id="1c757-128">Oggetto snapshot da rimuovere</span><span class="sxs-lookup"><span data-stu-id="1c757-128">The snapshot object to remove</span></span>

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

### <span data-ttu-id="1c757-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1c757-129">-Location</span></span>
<span data-ttu-id="1c757-130">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="1c757-130">The location of the resource</span></span>

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

### <span data-ttu-id="1c757-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="1c757-131">-MonthlySchedule</span></span>
<span data-ttu-id="1c757-132">Matrice Hashtable che rappresenta la pianificazione mensile</span><span class="sxs-lookup"><span data-stu-id="1c757-132">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="1c757-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c757-133">-Name</span></span>
<span data-ttu-id="1c757-134">Nome dei criteri di snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="1c757-134">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="1c757-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c757-135">-ResourceGroupName</span></span>
<span data-ttu-id="1c757-136">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="1c757-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1c757-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c757-137">-ResourceId</span></span>
<span data-ttu-id="1c757-138">ID risorsa dei criteri di snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="1c757-138">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="1c757-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c757-139">-Tag</span></span>
<span data-ttu-id="1c757-140">Matrice Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="1c757-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="1c757-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="1c757-141">-WeeklySchedule</span></span>
<span data-ttu-id="1c757-142">Matrice Hashtable che rappresenta la pianificazione mensile</span><span class="sxs-lookup"><span data-stu-id="1c757-142">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="1c757-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c757-143">-Confirm</span></span>
<span data-ttu-id="1c757-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c757-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c757-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c757-145">-WhatIf</span></span>
<span data-ttu-id="1c757-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c757-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c757-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c757-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c757-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c757-148">CommonParameters</span></span>
<span data-ttu-id="1c757-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c757-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c757-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c757-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c757-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c757-151">INPUTS</span></span>

### <span data-ttu-id="1c757-152">System. String</span><span class="sxs-lookup"><span data-stu-id="1c757-152">System.String</span></span>

### <span data-ttu-id="1c757-153">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1c757-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="1c757-154">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1c757-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1c757-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c757-155">OUTPUTS</span></span>

### <span data-ttu-id="1c757-156">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="1c757-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="1c757-157">Note</span><span class="sxs-lookup"><span data-stu-id="1c757-157">NOTES</span></span>

## <span data-ttu-id="1c757-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c757-158">RELATED LINKS</span></span>
