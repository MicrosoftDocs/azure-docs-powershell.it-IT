---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479271"
---
# <span data-ttu-id="83c83-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="83c83-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="83c83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83c83-102">SYNOPSIS</span></span>
<span data-ttu-id="83c83-103">Aggiorna un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="83c83-103">Updates a workspace.</span></span>

## <span data-ttu-id="83c83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83c83-104">SYNTAX</span></span>

### <span data-ttu-id="83c83-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83c83-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83c83-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83c83-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="83c83-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83c83-107">DESCRIPTION</span></span>
<span data-ttu-id="83c83-108">Aggiorna un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="83c83-108">Updates a workspace.</span></span>

## <span data-ttu-id="83c83-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83c83-109">EXAMPLES</span></span>

### <span data-ttu-id="83c83-110">Esempio 1: Aggiorna i tag di un'area di lavoro databricks</span><span class="sxs-lookup"><span data-stu-id="83c83-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="83c83-111">Questo comando Aggiorna i tag di un'area di lavoro databricks.</span><span class="sxs-lookup"><span data-stu-id="83c83-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="83c83-112">Esempio 2: abilitare la crittografia in un'area di lavoro databricks</span><span class="sxs-lookup"><span data-stu-id="83c83-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="83c83-113">L'attivazione della crittografia in un'area di lavoro databricks richiede tre passaggi:</span><span class="sxs-lookup"><span data-stu-id="83c83-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="83c83-114">Aggiornare l'area di lavoro con `-PrepareEncryption` (se non è stata creata così).</span><span class="sxs-lookup"><span data-stu-id="83c83-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="83c83-115">Trova `StorageAccountIdentityPrincipalId` nell'output dell'ultimo passaggio.</span><span class="sxs-lookup"><span data-stu-id="83c83-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="83c83-116">Concedere le autorizzazioni chiave per l'entità.</span><span class="sxs-lookup"><span data-stu-id="83c83-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="83c83-117">Aggiornare di nuovo l'area di lavoro per inserire informazioni sulla chiave di crittografia:</span><span class="sxs-lookup"><span data-stu-id="83c83-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="83c83-118">Esempio 3: disabilitare la crittografia in un'area di lavoro databricks</span><span class="sxs-lookup"><span data-stu-id="83c83-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="83c83-119">Per disabilitare la crittografia, è sufficiente impostarla `-EncryptionKeySource` su `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="83c83-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="83c83-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83c83-120">PARAMETERS</span></span>

### <span data-ttu-id="83c83-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83c83-121">-AsJob</span></span>
<span data-ttu-id="83c83-122">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="83c83-122">Run the command as a job</span></span>

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

### <span data-ttu-id="83c83-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c83-123">-DefaultProfile</span></span>
<span data-ttu-id="83c83-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83c83-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="83c83-125">-EncryptionKeyName</span></span>
<span data-ttu-id="83c83-126">Il nome della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="83c83-126">The name of Key Vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="83c83-127">-EncryptionKeySource</span></span>
<span data-ttu-id="83c83-128">Il provider di origine della crittografia.</span><span class="sxs-lookup"><span data-stu-id="83c83-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="83c83-129">Valori possibili (senza distinzione tra maiuscole e minuscole): default, Microsoft. Vault</span><span class="sxs-lookup"><span data-stu-id="83c83-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="83c83-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="83c83-131">URI (nome DNS) del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="83c83-131">The URI (DNS name) of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="83c83-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="83c83-133">La versione di Key Vault.</span><span class="sxs-lookup"><span data-stu-id="83c83-133">The version of KeyVault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83c83-134">-InputObject</span></span>
<span data-ttu-id="83c83-135">Parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="83c83-135">Identity parameter.</span></span>
<span data-ttu-id="83c83-136">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="83c83-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="83c83-137">-Name</span></span>
<span data-ttu-id="83c83-138">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="83c83-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-139">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="83c83-139">-NoWait</span></span>
<span data-ttu-id="83c83-140">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="83c83-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83c83-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="83c83-141">-PrepareEncryption</span></span>
<span data-ttu-id="83c83-142">Preparare l'area di lavoro per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="83c83-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="83c83-143">Abilita l'identità gestita per l'account di archiviazione gestita.</span><span class="sxs-lookup"><span data-stu-id="83c83-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="83c83-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83c83-144">-ResourceGroupName</span></span>
<span data-ttu-id="83c83-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83c83-145">The name of the resource group.</span></span>
<span data-ttu-id="83c83-146">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="83c83-146">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83c83-147">-SubscriptionId</span></span>
<span data-ttu-id="83c83-148">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="83c83-148">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="83c83-149">-Tag</span></span>
<span data-ttu-id="83c83-150">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="83c83-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c83-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83c83-151">-Confirm</span></span>
<span data-ttu-id="83c83-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83c83-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83c83-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83c83-153">-WhatIf</span></span>
<span data-ttu-id="83c83-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83c83-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83c83-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83c83-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83c83-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c83-156">CommonParameters</span></span>
<span data-ttu-id="83c83-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c83-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c83-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83c83-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c83-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83c83-159">INPUTS</span></span>

### <span data-ttu-id="83c83-160">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="83c83-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="83c83-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83c83-161">OUTPUTS</span></span>

### <span data-ttu-id="83c83-162">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="83c83-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="83c83-163">Note</span><span class="sxs-lookup"><span data-stu-id="83c83-163">NOTES</span></span>

<span data-ttu-id="83c83-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="83c83-164">ALIASES</span></span>

<span data-ttu-id="83c83-165">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83c83-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83c83-166">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="83c83-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83c83-167">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83c83-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83c83-168">INPUTOBJECT <IDatabricksIdentity> : parametro Identity.</span><span class="sxs-lookup"><span data-stu-id="83c83-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="83c83-169">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="83c83-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83c83-170">`[PeeringName <String>]`: Nome dell'area di lavoro vNet peering.</span><span class="sxs-lookup"><span data-stu-id="83c83-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="83c83-171">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83c83-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="83c83-172">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="83c83-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="83c83-173">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="83c83-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="83c83-174">`[WorkspaceName <String>]`: Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="83c83-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="83c83-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83c83-175">RELATED LINKS</span></span>

