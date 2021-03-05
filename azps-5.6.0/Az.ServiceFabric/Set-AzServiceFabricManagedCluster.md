---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 8a3ca4ed215dccbcc3cbfb541d7e023871bf6490
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005358"
---
# <span data-ttu-id="0177a-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0177a-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="0177a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0177a-102">SYNOPSIS</span></span>
<span data-ttu-id="0177a-103">Impostare le proprietà delle risorse cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="0177a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0177a-104">SYNTAX</span></span>

### <span data-ttu-id="0177a-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0177a-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0177a-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="0177a-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0177a-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="0177a-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0177a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0177a-108">DESCRIPTION</span></span>
<span data-ttu-id="0177a-109">Impostare le proprietà delle risorse cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="0177a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0177a-110">EXAMPLES</span></span>

### <span data-ttu-id="0177a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0177a-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="0177a-112">Aggiornare il nome DNS e la porta di connessione client per il cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="0177a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0177a-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="0177a-114">Aggiornare il nome DNS e la porta di connessione client per il cluster, con piping.</span><span class="sxs-lookup"><span data-stu-id="0177a-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="0177a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0177a-115">PARAMETERS</span></span>

### <span data-ttu-id="0177a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0177a-116">-AsJob</span></span>
<span data-ttu-id="0177a-117">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="0177a-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0177a-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="0177a-118">-ClientConnectionPort</span></span>
<span data-ttu-id="0177a-119">Porta utilizzata per le connessioni client al cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="0177a-120">Impostazione predefinita: 19000.</span><span class="sxs-lookup"><span data-stu-id="0177a-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="0177a-121">-CodeVersion</span></span>
<span data-ttu-id="0177a-122">Versione del codice cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-122">Cluster code version.</span></span> <span data-ttu-id="0177a-123">Usare solo se la modalità di aggiornamento è manuale.</span><span class="sxs-lookup"><span data-stu-id="0177a-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0177a-124">-DefaultProfile</span></span>
<span data-ttu-id="0177a-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0177a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0177a-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="0177a-126">-DnsName</span></span>
<span data-ttu-id="0177a-127">Nome DNS del cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="0177a-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="0177a-129">Porta utilizzata per le connessioni http al cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="0177a-130">Impostazione predefinita: 19080.</span><span class="sxs-lookup"><span data-stu-id="0177a-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0177a-131">-InputObject</span></span>
<span data-ttu-id="0177a-132">Risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="0177a-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="0177a-133">-Name</span></span>
<span data-ttu-id="0177a-134">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0177a-135">-ResourceGroupName</span></span>
<span data-ttu-id="0177a-136">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0177a-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0177a-137">-ResourceId</span></span>
<span data-ttu-id="0177a-138">ID risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="0177a-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="0177a-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="0177a-140">Endpoint utilizzato dal proxy inverso.</span><span class="sxs-lookup"><span data-stu-id="0177a-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="0177a-141">-UpgradeMode</span></span>
<span data-ttu-id="0177a-142">Modalità di aggiornamento della versione del codice cluster.</span><span class="sxs-lookup"><span data-stu-id="0177a-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="0177a-143">Automatico o Manuale.</span><span class="sxs-lookup"><span data-stu-id="0177a-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0177a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0177a-144">-Confirm</span></span>
<span data-ttu-id="0177a-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0177a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0177a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0177a-146">-WhatIf</span></span>
<span data-ttu-id="0177a-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0177a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0177a-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0177a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0177a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0177a-149">CommonParameters</span></span>
<span data-ttu-id="0177a-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0177a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0177a-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0177a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0177a-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="0177a-152">INPUTS</span></span>

### <span data-ttu-id="0177a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0177a-153">System.String</span></span>

## <span data-ttu-id="0177a-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0177a-154">OUTPUTS</span></span>

### <span data-ttu-id="0177a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0177a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="0177a-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="0177a-156">NOTES</span></span>

## <span data-ttu-id="0177a-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0177a-157">RELATED LINKS</span></span>
