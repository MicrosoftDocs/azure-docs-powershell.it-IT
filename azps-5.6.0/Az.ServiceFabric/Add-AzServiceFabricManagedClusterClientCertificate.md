---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: 11534ff7102295cd312410c5ecbae932fd9459e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969838"
---
# <span data-ttu-id="8d42a-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8d42a-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="8d42a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d42a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d42a-103">Aggiungere il nome comune del certificato o l'impronta digitale al cluster.</span><span class="sxs-lookup"><span data-stu-id="8d42a-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="8d42a-104">Il certificato verrà registrato di nuovo nel cluster ai fini dell'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="8d42a-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="8d42a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d42a-105">SYNTAX</span></span>

### <span data-ttu-id="8d42a-106">ClientCertByTpByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8d42a-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d42a-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="8d42a-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d42a-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="8d42a-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d42a-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="8d42a-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d42a-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d42a-110">DESCRIPTION</span></span>
<span data-ttu-id="8d42a-111">Aggiungere il nome comune del certificato o l'impronta digitale al cluster.</span><span class="sxs-lookup"><span data-stu-id="8d42a-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="8d42a-112">Il certificato verrà registrato di nuovo nel cluster ai fini dell'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="8d42a-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="8d42a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d42a-113">EXAMPLES</span></span>

### <span data-ttu-id="8d42a-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d42a-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="8d42a-115">Questo comando aggiunge il certificato con immagine thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' al cluster, in modo che il client possa usare il certificato come amministratore per comunicare con il cluster.</span><span class="sxs-lookup"><span data-stu-id="8d42a-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="8d42a-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8d42a-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="8d42a-117">Questo comando aggiungerà un certificato client di sola lettura con nome comune "Contoso.com" e 2 autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="8d42a-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="8d42a-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8d42a-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="8d42a-119">Questo comando aggiunge un certificato client di sola lettura con nome comune "Contoso.com" e 2 autorità di certificazione, con piping.</span><span class="sxs-lookup"><span data-stu-id="8d42a-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="8d42a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d42a-120">PARAMETERS</span></span>

### <span data-ttu-id="8d42a-121">-Admin</span><span class="sxs-lookup"><span data-stu-id="8d42a-121">-Admin</span></span>
<span data-ttu-id="8d42a-122">Consente di specificare se il certificato client ha il livello di amministratore.</span><span class="sxs-lookup"><span data-stu-id="8d42a-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="8d42a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d42a-123">-AsJob</span></span>
<span data-ttu-id="8d42a-124">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="8d42a-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8d42a-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="8d42a-125">-CommonName</span></span>
<span data-ttu-id="8d42a-126">Nome comune certificato client.</span><span class="sxs-lookup"><span data-stu-id="8d42a-126">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d42a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d42a-127">-DefaultProfile</span></span>
<span data-ttu-id="8d42a-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d42a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d42a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d42a-129">-InputObject</span></span>
<span data-ttu-id="8d42a-130">Risorsa cluster gestita</span><span class="sxs-lookup"><span data-stu-id="8d42a-130">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d42a-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="8d42a-131">-IssuerThumbprint</span></span>
<span data-ttu-id="8d42a-132">Elenco delle identificazioni in pollice dell'autorità di certificazione per il certificato client.</span><span class="sxs-lookup"><span data-stu-id="8d42a-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="8d42a-133">Usare solo in combinazione con CommonName.</span><span class="sxs-lookup"><span data-stu-id="8d42a-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d42a-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8d42a-134">-Name</span></span>
<span data-ttu-id="8d42a-135">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="8d42a-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d42a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d42a-136">-ResourceGroupName</span></span>
<span data-ttu-id="8d42a-137">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8d42a-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d42a-138">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="8d42a-138">-Thumbprint</span></span>
<span data-ttu-id="8d42a-139">Pollice in pollice del certificato client.</span><span class="sxs-lookup"><span data-stu-id="8d42a-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d42a-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d42a-140">-Confirm</span></span>
<span data-ttu-id="8d42a-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d42a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d42a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d42a-142">-WhatIf</span></span>
<span data-ttu-id="8d42a-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d42a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d42a-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d42a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d42a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d42a-145">CommonParameters</span></span>
<span data-ttu-id="8d42a-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d42a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d42a-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d42a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d42a-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d42a-148">INPUTS</span></span>

### <span data-ttu-id="8d42a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8d42a-149">System.String</span></span>

## <span data-ttu-id="8d42a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d42a-150">OUTPUTS</span></span>

### <span data-ttu-id="8d42a-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="8d42a-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="8d42a-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d42a-152">NOTES</span></span>

## <span data-ttu-id="8d42a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d42a-153">RELATED LINKS</span></span>
