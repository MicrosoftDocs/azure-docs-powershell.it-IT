---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193640"
---
# <span data-ttu-id="4a7c2-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="4a7c2-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="4a7c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a7c2-103">Aggiungere il segreto del certificato al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="4a7c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a7c2-104">SYNTAX</span></span>

### <span data-ttu-id="4a7c2-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a7c2-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a7c2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4a7c2-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a7c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a7c2-107">DESCRIPTION</span></span>
<span data-ttu-id="4a7c2-108">Aggiungere il segreto del certificato al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="4a7c2-109">Il segreto deve essere archiviato in un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="4a7c2-110">Per altre informazioni relative a Key Vault, vedere cos'è Azure Key Vault?</span><span class="sxs-lookup"><span data-stu-id="4a7c2-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="4a7c2-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="4a7c2-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="4a7c2-112">Per altre informazioni sui cmdlet, vedere cmdlet di Key Vault di Azure ( https://msdn.microsoft.com/library/azure/dn868052.aspx) nella raccolta di Microsoft Developer Network o nel cmdlet Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="4a7c2-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a7c2-113">EXAMPLES</span></span>

### <span data-ttu-id="4a7c2-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a7c2-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="4a7c2-115">La virgola Aggiunge un certificato segreto dall'identificatore segreto e della volta specificato.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="4a7c2-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4a7c2-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="4a7c2-117">Questa virgola Aggiunge un certificato segreto dall'identificatore segreto e della volta specificato, con piping.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="4a7c2-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a7c2-118">PARAMETERS</span></span>

### <span data-ttu-id="4a7c2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a7c2-119">-AsJob</span></span>
<span data-ttu-id="4a7c2-120">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4a7c2-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="4a7c2-121">-CertificateStore</span></span>
<span data-ttu-id="4a7c2-122">Specifica l'archivio certificati nella macchina virtuale a cui deve essere aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="4a7c2-123">L'archivio certificati specificato è implicitamente nell'account LocalMachine.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="4a7c2-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="4a7c2-124">-CertificateUrl</span></span>
<span data-ttu-id="4a7c2-125">Questo è l'URL di un certificato caricato in Key Vault come segreto.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="4a7c2-126">Per aggiungere un segreto alla chiave di volta, vedere \[ aggiungere una chiave o un segreto al Vault chiave \] ( https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="4a7c2-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="4a7c2-127">In questo caso, è necessario che il certificato sia la codifica Base64 dell'oggetto JSON seguente codificato in UTF-8: \<br\> \<br\> { \<br\> "dati": " \<Base64-encoded-certificate\> ", \<br\> "tipo": "pfx", \<br\> "password": " \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="4a7c2-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="4a7c2-128">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4a7c2-128">-ClusterName</span></span>
<span data-ttu-id="4a7c2-129">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4a7c2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a7c2-130">-DefaultProfile</span></span>
<span data-ttu-id="4a7c2-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a7c2-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a7c2-132">-InputObject</span></span>
<span data-ttu-id="4a7c2-133">Risorsa tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="4a7c2-133">Node Type resource</span></span>

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

### <span data-ttu-id="4a7c2-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a7c2-134">-Name</span></span>
<span data-ttu-id="4a7c2-135">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="4a7c2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a7c2-136">-ResourceGroupName</span></span>
<span data-ttu-id="4a7c2-137">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4a7c2-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4a7c2-138">-SourceVaultId</span></span>
<span data-ttu-id="4a7c2-139">ID risorsa chiave del Vault contenente i certificati.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="4a7c2-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a7c2-140">-Confirm</span></span>
<span data-ttu-id="4a7c2-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a7c2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a7c2-142">-WhatIf</span></span>
<span data-ttu-id="4a7c2-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a7c2-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a7c2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a7c2-145">CommonParameters</span></span>
<span data-ttu-id="4a7c2-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a7c2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a7c2-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a7c2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a7c2-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a7c2-148">INPUTS</span></span>

### <span data-ttu-id="4a7c2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4a7c2-149">System.String</span></span>

## <span data-ttu-id="4a7c2-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a7c2-150">OUTPUTS</span></span>

### <span data-ttu-id="4a7c2-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="4a7c2-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="4a7c2-152">Note</span><span class="sxs-lookup"><span data-stu-id="4a7c2-152">NOTES</span></span>

## <span data-ttu-id="4a7c2-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a7c2-153">RELATED LINKS</span></span>
