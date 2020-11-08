---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191912"
---
# <span data-ttu-id="d66ac-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d66ac-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="d66ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d66ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d66ac-103">Remvoe certificato client per identificazione personale o nome comune.</span><span class="sxs-lookup"><span data-stu-id="d66ac-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="d66ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d66ac-104">SYNTAX</span></span>

### <span data-ttu-id="d66ac-105">ClientCertByTpByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d66ac-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66ac-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="d66ac-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d66ac-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="d66ac-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d66ac-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="d66ac-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d66ac-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d66ac-109">DESCRIPTION</span></span>
<span data-ttu-id="d66ac-110">Remvoe certificato client per identificazione personale o nome comune.</span><span class="sxs-lookup"><span data-stu-id="d66ac-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="d66ac-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d66ac-111">EXAMPLES</span></span>

### <span data-ttu-id="d66ac-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d66ac-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="d66ac-113">Rimuovere il certificato client in base al nome comune.</span><span class="sxs-lookup"><span data-stu-id="d66ac-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="d66ac-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d66ac-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d66ac-115">Rimuovere il certificato client in base all'identificazione personale.</span><span class="sxs-lookup"><span data-stu-id="d66ac-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="d66ac-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d66ac-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d66ac-117">Rimuovere il certificato client in base all'identificazione personale, con piping.</span><span class="sxs-lookup"><span data-stu-id="d66ac-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="d66ac-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d66ac-118">PARAMETERS</span></span>

### <span data-ttu-id="d66ac-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d66ac-119">-AsJob</span></span>
<span data-ttu-id="d66ac-120">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="d66ac-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d66ac-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="d66ac-121">-CommonName</span></span>
<span data-ttu-id="d66ac-122">Nome comune del certificato client.</span><span class="sxs-lookup"><span data-stu-id="d66ac-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="d66ac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66ac-123">-DefaultProfile</span></span>
<span data-ttu-id="d66ac-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d66ac-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66ac-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d66ac-125">-InputObject</span></span>
<span data-ttu-id="d66ac-126">Risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="d66ac-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="d66ac-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d66ac-127">-Name</span></span>
<span data-ttu-id="d66ac-128">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="d66ac-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66ac-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d66ac-129">-PassThru</span></span>
<span data-ttu-id="d66ac-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d66ac-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d66ac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66ac-131">-ResourceGroupName</span></span>
<span data-ttu-id="d66ac-132">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d66ac-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66ac-133">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="d66ac-133">-Thumbprint</span></span>
<span data-ttu-id="d66ac-134">Identificazione personale del certificato client.</span><span class="sxs-lookup"><span data-stu-id="d66ac-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66ac-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d66ac-135">-Confirm</span></span>
<span data-ttu-id="d66ac-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d66ac-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d66ac-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66ac-137">-WhatIf</span></span>
<span data-ttu-id="d66ac-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d66ac-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d66ac-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d66ac-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d66ac-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66ac-140">CommonParameters</span></span>
<span data-ttu-id="d66ac-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d66ac-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66ac-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d66ac-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66ac-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d66ac-143">INPUTS</span></span>

### <span data-ttu-id="d66ac-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d66ac-144">System.String</span></span>

## <span data-ttu-id="d66ac-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d66ac-145">OUTPUTS</span></span>

### <span data-ttu-id="d66ac-146">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d66ac-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d66ac-147">Note</span><span class="sxs-lookup"><span data-stu-id="d66ac-147">NOTES</span></span>

## <span data-ttu-id="d66ac-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d66ac-148">RELATED LINKS</span></span>