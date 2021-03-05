---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 14c2a58c40aa29f1b48902be5d82911f70a71cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968125"
---
# <span data-ttu-id="fbaef-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fbaef-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="fbaef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbaef-102">SYNOPSIS</span></span>
<span data-ttu-id="fbaef-103">Aggiorna un criterio di backup dei file ANF di Azure ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="fbaef-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="fbaef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbaef-104">SYNTAX</span></span>

### <span data-ttu-id="fbaef-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fbaef-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbaef-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbaef-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbaef-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbaef-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbaef-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbaef-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbaef-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fbaef-109">DESCRIPTION</span></span>
<span data-ttu-id="fbaef-110">Il cmdlet **Update-AzNetAppFilesBackupPolicy** modifica un criterio di backup ANF.</span><span class="sxs-lookup"><span data-stu-id="fbaef-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="fbaef-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbaef-111">EXAMPLES</span></span>

### <span data-ttu-id="fbaef-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fbaef-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="fbaef-113">Questo comando modifica il criterio di backup ANF "MyBackupPolicy" in modo che abbia il dato DailyBackupsToKeep.</span><span class="sxs-lookup"><span data-stu-id="fbaef-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="fbaef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbaef-114">PARAMETERS</span></span>

### <span data-ttu-id="fbaef-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fbaef-115">-AccountName</span></span>
<span data-ttu-id="fbaef-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="fbaef-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="fbaef-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="fbaef-117">-AccountObject</span></span>
<span data-ttu-id="fbaef-118">Oggetto Account contenente il criterio di backup da aggiornare</span><span class="sxs-lookup"><span data-stu-id="fbaef-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="fbaef-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="fbaef-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="fbaef-120">I backup giornalieri sono da conservare</span><span class="sxs-lookup"><span data-stu-id="fbaef-120">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbaef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbaef-121">-DefaultProfile</span></span>
<span data-ttu-id="fbaef-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbaef-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbaef-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbaef-123">-InputObject</span></span>
<span data-ttu-id="fbaef-124">Oggetto BackupPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="fbaef-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaef-125">-Location</span><span class="sxs-lookup"><span data-stu-id="fbaef-125">-Location</span></span>
<span data-ttu-id="fbaef-126">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="fbaef-126">The location of the resource</span></span>

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

### <span data-ttu-id="fbaef-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="fbaef-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="fbaef-128">Conteggio dei backup mensili da conservare</span><span class="sxs-lookup"><span data-stu-id="fbaef-128">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbaef-129">-Name</span><span class="sxs-lookup"><span data-stu-id="fbaef-129">-Name</span></span>
<span data-ttu-id="fbaef-130">Nome dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="fbaef-130">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbaef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbaef-131">-ResourceGroupName</span></span>
<span data-ttu-id="fbaef-132">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="fbaef-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="fbaef-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbaef-133">-ResourceId</span></span>
<span data-ttu-id="fbaef-134">ID risorsa dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="fbaef-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="fbaef-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbaef-135">-Tag</span></span>
<span data-ttu-id="fbaef-136">Matrice di tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="fbaef-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="fbaef-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="fbaef-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="fbaef-138">Conteggio dei backup settimanali da conservare</span><span class="sxs-lookup"><span data-stu-id="fbaef-138">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbaef-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="fbaef-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="fbaef-140">Numero di backup annuale da conservare</span><span class="sxs-lookup"><span data-stu-id="fbaef-140">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbaef-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbaef-141">-Confirm</span></span>
<span data-ttu-id="fbaef-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbaef-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbaef-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbaef-143">-WhatIf</span></span>
<span data-ttu-id="fbaef-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbaef-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbaef-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbaef-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbaef-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbaef-146">CommonParameters</span></span>
<span data-ttu-id="fbaef-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbaef-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbaef-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fbaef-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbaef-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="fbaef-149">INPUTS</span></span>

### <span data-ttu-id="fbaef-150">System.String</span><span class="sxs-lookup"><span data-stu-id="fbaef-150">System.String</span></span>

### <span data-ttu-id="fbaef-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="fbaef-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="fbaef-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fbaef-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="fbaef-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbaef-153">OUTPUTS</span></span>

### <span data-ttu-id="fbaef-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fbaef-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="fbaef-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="fbaef-155">NOTES</span></span>

## <span data-ttu-id="fbaef-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbaef-156">RELATED LINKS</span></span>
