---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208018"
---
# <span data-ttu-id="11a92-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="11a92-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="11a92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11a92-102">SYNOPSIS</span></span>
<span data-ttu-id="11a92-103">Creare un nuovo cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="11a92-103">Create new managed cluster.</span></span>

## <span data-ttu-id="11a92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11a92-104">SYNTAX</span></span>

### <span data-ttu-id="11a92-105">ClientCertByTp (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11a92-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11a92-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="11a92-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11a92-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="11a92-107">DESCRIPTION</span></span>
<span data-ttu-id="11a92-108">Questo cmdlet creerà una risorsa cluster gestita senza tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="11a92-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="11a92-109">Per avviare il programma di avvio del cluster È necessario aggiungere un tipo di nodo primario con [New-AzServiceFabricManagedNodeType.](./New-AzServiceFabricManagedNodeType.md)</span><span class="sxs-lookup"><span data-stu-id="11a92-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="11a92-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11a92-110">EXAMPLES</span></span>

### <span data-ttu-id="11a92-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="11a92-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="11a92-112">Questo comando crea una risorsa cluster con SKU di base predefinite.</span><span class="sxs-lookup"><span data-stu-id="11a92-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="11a92-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="11a92-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="11a92-114">Questo comando crea una risorsa cluster in centraluseuap con un certificato client di amministrazione iniziale e una SKU standard.</span><span class="sxs-lookup"><span data-stu-id="11a92-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="11a92-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11a92-115">PARAMETERS</span></span>

### <span data-ttu-id="11a92-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="11a92-116">-AdminPassword</span></span>
<span data-ttu-id="11a92-117">Password di amministratore usata per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="11a92-117">Admin password used for the virtual machines.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="11a92-118">-AdminUserName</span></span>
<span data-ttu-id="11a92-119">Password di amministratore usata per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="11a92-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="11a92-120">Impostazione predefinita: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="11a92-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11a92-121">-AsJob</span></span>
<span data-ttu-id="11a92-122">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="11a92-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="11a92-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="11a92-123">-ClientCertCommonName</span></span>
<span data-ttu-id="11a92-124">Nome comune certificato client.</span><span class="sxs-lookup"><span data-stu-id="11a92-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="11a92-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="11a92-126">Consente di specificare se il certificato client ha il livello di amministratore.</span><span class="sxs-lookup"><span data-stu-id="11a92-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="11a92-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="11a92-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="11a92-128">Elenco di pollice in pollice dell'autorità di certificazione per il certificato client.</span><span class="sxs-lookup"><span data-stu-id="11a92-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="11a92-129">Da usare solo in combinazione con ClientCertCommonName.</span><span class="sxs-lookup"><span data-stu-id="11a92-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="11a92-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="11a92-131">Pollice in pollice del certificato client.</span><span class="sxs-lookup"><span data-stu-id="11a92-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="11a92-132">-ClientConnectionPort</span></span>
<span data-ttu-id="11a92-133">Porta utilizzata per le connessioni client al cluster.</span><span class="sxs-lookup"><span data-stu-id="11a92-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="11a92-134">Impostazione predefinita: 19000.</span><span class="sxs-lookup"><span data-stu-id="11a92-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="11a92-135">-CodeVersion</span></span>
<span data-ttu-id="11a92-136">Versione del codice dell'infrastruttura del servizio cluster.</span><span class="sxs-lookup"><span data-stu-id="11a92-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="11a92-137">Usare solo se la modalità di aggiornamento è manuale.</span><span class="sxs-lookup"><span data-stu-id="11a92-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="11a92-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a92-138">-DefaultProfile</span></span>
<span data-ttu-id="11a92-139">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11a92-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11a92-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="11a92-140">-DnsName</span></span>
<span data-ttu-id="11a92-141">Nome DNS del cluster.</span><span class="sxs-lookup"><span data-stu-id="11a92-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="11a92-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="11a92-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="11a92-143">Porta utilizzata per le connessioni http al cluster.</span><span class="sxs-lookup"><span data-stu-id="11a92-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="11a92-144">Impostazione predefinita: 19080.</span><span class="sxs-lookup"><span data-stu-id="11a92-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-145">-Location</span><span class="sxs-lookup"><span data-stu-id="11a92-145">-Location</span></span>
<span data-ttu-id="11a92-146">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="11a92-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-147">-Name</span><span class="sxs-lookup"><span data-stu-id="11a92-147">-Name</span></span>
<span data-ttu-id="11a92-148">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="11a92-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a92-149">-ResourceGroupName</span></span>
<span data-ttu-id="11a92-150">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11a92-150">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="11a92-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="11a92-152">Endpoint utilizzato dal proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="11a92-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="11a92-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="11a92-153">-Sku</span></span>
<span data-ttu-id="11a92-154">SKU del cluster, le opzioni sono di base: avrà un minimo di 3 nodi di seed e consente solo 1 tipo di nodo e Standard: avrà un minimo di 5 nodi seed e consente più tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="11a92-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="11a92-155">-UpgradeMode</span></span>
<span data-ttu-id="11a92-156">Modalità di aggiornamento della versione del codice dell'infrastruttura del servizio cluster.</span><span class="sxs-lookup"><span data-stu-id="11a92-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="11a92-157">Automatico o Manuale.</span><span class="sxs-lookup"><span data-stu-id="11a92-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a92-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="11a92-158">-UseTestExtension</span></span>
<span data-ttu-id="11a92-159">Se si specifica, il cluster verrà associato all'estensione vmss di test del servizio.</span><span class="sxs-lookup"><span data-stu-id="11a92-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="11a92-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11a92-160">-Confirm</span></span>
<span data-ttu-id="11a92-161">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11a92-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11a92-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11a92-162">-WhatIf</span></span>
<span data-ttu-id="11a92-163">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11a92-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11a92-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11a92-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11a92-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a92-165">CommonParameters</span></span>
<span data-ttu-id="11a92-166">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a92-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a92-167">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11a92-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a92-168">INPUT</span><span class="sxs-lookup"><span data-stu-id="11a92-168">INPUTS</span></span>

### <span data-ttu-id="11a92-169">System.String</span><span class="sxs-lookup"><span data-stu-id="11a92-169">System.String</span></span>

## <span data-ttu-id="11a92-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11a92-170">OUTPUTS</span></span>

### <span data-ttu-id="11a92-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="11a92-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="11a92-172">NOTE</span><span class="sxs-lookup"><span data-stu-id="11a92-172">NOTES</span></span>

## <span data-ttu-id="11a92-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11a92-173">RELATED LINKS</span></span>

[<span data-ttu-id="11a92-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="11a92-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)