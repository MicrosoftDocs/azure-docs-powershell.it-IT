---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380488"
---
# <span data-ttu-id="7c84f-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7c84f-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="7c84f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c84f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c84f-103">Aggiorna i criteri di backup di Azure NetApp Files (ANF) con i modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="7c84f-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="7c84f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c84f-104">SYNTAX</span></span>

### <span data-ttu-id="7c84f-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c84f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c84f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c84f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c84f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c84f-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c84f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c84f-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c84f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c84f-109">DESCRIPTION</span></span>
<span data-ttu-id="7c84f-110">Il cmdlet **Update-AzNetAppFilesBackupPolicy** modifica un criterio di backup di ANF.</span><span class="sxs-lookup"><span data-stu-id="7c84f-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="7c84f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c84f-111">EXAMPLES</span></span>

### <span data-ttu-id="7c84f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c84f-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="7c84f-113">Questo comando modifica il criterio di backup di ANF "MyBackupPolicy" per avere l'DailyBackupsToKeep specificata.</span><span class="sxs-lookup"><span data-stu-id="7c84f-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="7c84f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c84f-114">PARAMETERS</span></span>

### <span data-ttu-id="7c84f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7c84f-115">-AccountName</span></span>
<span data-ttu-id="7c84f-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="7c84f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="7c84f-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="7c84f-117">-AccountObject</span></span>
<span data-ttu-id="7c84f-118">L'oggetto account che contiene i criteri di backup da aggiornare</span><span class="sxs-lookup"><span data-stu-id="7c84f-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="7c84f-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="7c84f-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="7c84f-120">Conteggio backup giornalieri da conservare</span><span class="sxs-lookup"><span data-stu-id="7c84f-120">Daily backups count to keep</span></span>

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

### <span data-ttu-id="7c84f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c84f-121">-DefaultProfile</span></span>
<span data-ttu-id="7c84f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c84f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c84f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c84f-123">-InputObject</span></span>
<span data-ttu-id="7c84f-124">Oggetto BackupPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="7c84f-124">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="7c84f-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7c84f-125">-Location</span></span>
<span data-ttu-id="7c84f-126">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="7c84f-126">The location of the resource</span></span>

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

### <span data-ttu-id="7c84f-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="7c84f-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="7c84f-128">Numero di backup mensili da conservare</span><span class="sxs-lookup"><span data-stu-id="7c84f-128">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="7c84f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c84f-129">-Name</span></span>
<span data-ttu-id="7c84f-130">Nome del criterio di backup di ANF</span><span class="sxs-lookup"><span data-stu-id="7c84f-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="7c84f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c84f-131">-ResourceGroupName</span></span>
<span data-ttu-id="7c84f-132">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="7c84f-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7c84f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c84f-133">-ResourceId</span></span>
<span data-ttu-id="7c84f-134">ID risorsa dei criteri di backup di ANF</span><span class="sxs-lookup"><span data-stu-id="7c84f-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="7c84f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c84f-135">-Tag</span></span>
<span data-ttu-id="7c84f-136">Matrice Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="7c84f-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="7c84f-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="7c84f-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="7c84f-138">Conteggio backup settimanali da conservare</span><span class="sxs-lookup"><span data-stu-id="7c84f-138">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="7c84f-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="7c84f-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="7c84f-140">Numero di copie di backup annuali da conservare</span><span class="sxs-lookup"><span data-stu-id="7c84f-140">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="7c84f-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c84f-141">-Confirm</span></span>
<span data-ttu-id="7c84f-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c84f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c84f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c84f-143">-WhatIf</span></span>
<span data-ttu-id="7c84f-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c84f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c84f-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c84f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c84f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c84f-146">CommonParameters</span></span>
<span data-ttu-id="7c84f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c84f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c84f-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c84f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c84f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c84f-149">INPUTS</span></span>

### <span data-ttu-id="7c84f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7c84f-150">System.String</span></span>

### <span data-ttu-id="7c84f-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7c84f-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="7c84f-152">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7c84f-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="7c84f-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c84f-153">OUTPUTS</span></span>

### <span data-ttu-id="7c84f-154">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7c84f-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="7c84f-155">Note</span><span class="sxs-lookup"><span data-stu-id="7c84f-155">NOTES</span></span>

## <span data-ttu-id="7c84f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c84f-156">RELATED LINKS</span></span>
