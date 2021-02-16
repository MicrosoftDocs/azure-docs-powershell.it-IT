---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201574"
---
# <span data-ttu-id="b64c7-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="b64c7-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="b64c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b64c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b64c7-103">Aggiungere il segreto certificato al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="b64c7-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="b64c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b64c7-104">SYNTAX</span></span>

### <span data-ttu-id="b64c7-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b64c7-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b64c7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b64c7-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b64c7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b64c7-107">DESCRIPTION</span></span>
<span data-ttu-id="b64c7-108">Aggiungere il segreto certificato al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="b64c7-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="b64c7-109">Il segreto deve essere archiviato in un Vault chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="b64c7-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="b64c7-110">Per altre informazioni relative al Vault delle chiavi, vedere Che cos'è il Vault delle chiavi di Azure?</span><span class="sxs-lookup"><span data-stu-id="b64c7-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="b64c7-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="b64c7-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="b64c7-112">Per altre informazioni sui cmdlet, vedere i cmdlet del Vault delle chiavi di Azure ( nella libreria https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft Developer Network o nel cmdlet Set-AzKeyVaultSecret></span><span class="sxs-lookup"><span data-stu-id="b64c7-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="b64c7-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b64c7-113">EXAMPLES</span></span>

### <span data-ttu-id="b64c7-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b64c7-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="b64c7-115">Questo punto e virgola aggiunge un certificato segreto dalla chiave e dall'identificatore segreto specificati.</span><span class="sxs-lookup"><span data-stu-id="b64c7-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="b64c7-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b64c7-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="b64c7-117">Questo punto e virgola aggiunge un certificato segreto dall'identificatore segreto specificato, con piping.</span><span class="sxs-lookup"><span data-stu-id="b64c7-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="b64c7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b64c7-118">PARAMETERS</span></span>

### <span data-ttu-id="b64c7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b64c7-119">-AsJob</span></span>
<span data-ttu-id="b64c7-120">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b64c7-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b64c7-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="b64c7-121">-CertificateStore</span></span>
<span data-ttu-id="b64c7-122">Specifica l'archivio certificati nella macchina virtuale a cui aggiungere il certificato.</span><span class="sxs-lookup"><span data-stu-id="b64c7-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="b64c7-123">L'archivio certificati specificato è implicito nell'account LocalMachine.</span><span class="sxs-lookup"><span data-stu-id="b64c7-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64c7-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b64c7-124">-CertificateUrl</span></span>
<span data-ttu-id="b64c7-125">URL di un certificato che è stato caricato come segreto nel Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="b64c7-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="b64c7-126">Per aggiungere un segreto al Vault delle chiavi, vedere Aggiungere una chiave o un segreto \[ al vault della chiave ( \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="b64c7-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="b64c7-127">In questo caso, il certificato deve essere la codifica Base64 dell'oggetto JSON seguente codificato in UTF-8: \<br\> \<br\> { \<br\> "data":" \<Base64-encoded-certificate\> ", \<br\> "dataType":"pfx", \<br\> "password":" \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="b64c7-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64c7-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b64c7-128">-ClusterName</span></span>
<span data-ttu-id="b64c7-129">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="b64c7-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b64c7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64c7-130">-DefaultProfile</span></span>
<span data-ttu-id="b64c7-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b64c7-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b64c7-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b64c7-132">-InputObject</span></span>
<span data-ttu-id="b64c7-133">Risorsa Tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="b64c7-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b64c7-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b64c7-134">-Name</span></span>
<span data-ttu-id="b64c7-135">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="b64c7-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b64c7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b64c7-136">-ResourceGroupName</span></span>
<span data-ttu-id="b64c7-137">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b64c7-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b64c7-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b64c7-138">-SourceVaultId</span></span>
<span data-ttu-id="b64c7-139">ID risorsa vault chiave contenente i certificati.</span><span class="sxs-lookup"><span data-stu-id="b64c7-139">Key Vault resource id containing the certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64c7-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b64c7-140">-Confirm</span></span>
<span data-ttu-id="b64c7-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b64c7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b64c7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b64c7-142">-WhatIf</span></span>
<span data-ttu-id="b64c7-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b64c7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b64c7-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b64c7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b64c7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64c7-145">CommonParameters</span></span>
<span data-ttu-id="b64c7-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b64c7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64c7-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b64c7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64c7-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="b64c7-148">INPUTS</span></span>

### <span data-ttu-id="b64c7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b64c7-149">System.String</span></span>

## <span data-ttu-id="b64c7-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b64c7-150">OUTPUTS</span></span>

### <span data-ttu-id="b64c7-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="b64c7-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="b64c7-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="b64c7-152">NOTES</span></span>

## <span data-ttu-id="b64c7-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b64c7-153">RELATED LINKS</span></span>
