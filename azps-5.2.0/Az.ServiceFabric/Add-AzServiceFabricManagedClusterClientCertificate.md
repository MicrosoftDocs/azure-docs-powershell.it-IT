---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348652"
---
# <span data-ttu-id="37d6f-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="37d6f-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="37d6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="37d6f-103">Aggiungere al cluster il nome comune o l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="37d6f-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="37d6f-104">Verrà registrato di nuovo il certificato per scopi di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="37d6f-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="37d6f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37d6f-105">SYNTAX</span></span>

### <span data-ttu-id="37d6f-106">ClientCertByTpByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37d6f-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37d6f-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="37d6f-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37d6f-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="37d6f-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d6f-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="37d6f-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d6f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37d6f-110">DESCRIPTION</span></span>
<span data-ttu-id="37d6f-111">Aggiungere al cluster il nome comune o l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="37d6f-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="37d6f-112">Verrà registrato di nuovo il certificato per scopi di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="37d6f-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="37d6f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37d6f-113">EXAMPLES</span></span>

### <span data-ttu-id="37d6f-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37d6f-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="37d6f-115">Questo comando aggiungerà il certificato con l'identificazione personale "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" al cluster, in modo che il client possa usare il certificato come amministratore per comunicare con il cluster.</span><span class="sxs-lookup"><span data-stu-id="37d6f-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="37d6f-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="37d6f-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="37d6f-117">Questo comando aggiungerà un certificato client di sola lettura con nome comune "Contoso.com" e 2 emittenti.</span><span class="sxs-lookup"><span data-stu-id="37d6f-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="37d6f-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="37d6f-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="37d6f-119">Questo comando aggiungerà un certificato client di sola lettura con il nome comune ' Contoso.com ' e due emittenti con piping.</span><span class="sxs-lookup"><span data-stu-id="37d6f-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="37d6f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37d6f-120">PARAMETERS</span></span>

### <span data-ttu-id="37d6f-121">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="37d6f-121">-Admin</span></span>
<span data-ttu-id="37d6f-122">Consente di specificare se il certificato client ha un livello di amministratore.</span><span class="sxs-lookup"><span data-stu-id="37d6f-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="37d6f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37d6f-123">-AsJob</span></span>
<span data-ttu-id="37d6f-124">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="37d6f-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="37d6f-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="37d6f-125">-CommonName</span></span>
<span data-ttu-id="37d6f-126">Nome comune del certificato client.</span><span class="sxs-lookup"><span data-stu-id="37d6f-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="37d6f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d6f-127">-DefaultProfile</span></span>
<span data-ttu-id="37d6f-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37d6f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37d6f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37d6f-129">-InputObject</span></span>
<span data-ttu-id="37d6f-130">Risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="37d6f-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="37d6f-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="37d6f-131">-IssuerThumbprint</span></span>
<span data-ttu-id="37d6f-132">Elenco delle identificazioni personali dell'autorità di certificazione per il certificato client.</span><span class="sxs-lookup"><span data-stu-id="37d6f-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="37d6f-133">Usare solo in combinazione con CommonName.</span><span class="sxs-lookup"><span data-stu-id="37d6f-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="37d6f-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="37d6f-134">-Name</span></span>
<span data-ttu-id="37d6f-135">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="37d6f-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="37d6f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d6f-136">-ResourceGroupName</span></span>
<span data-ttu-id="37d6f-137">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37d6f-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="37d6f-138">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="37d6f-138">-Thumbprint</span></span>
<span data-ttu-id="37d6f-139">Identificazione personale del certificato client.</span><span class="sxs-lookup"><span data-stu-id="37d6f-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="37d6f-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37d6f-140">-Confirm</span></span>
<span data-ttu-id="37d6f-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37d6f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37d6f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d6f-142">-WhatIf</span></span>
<span data-ttu-id="37d6f-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37d6f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37d6f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37d6f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37d6f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d6f-145">CommonParameters</span></span>
<span data-ttu-id="37d6f-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d6f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d6f-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37d6f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d6f-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37d6f-148">INPUTS</span></span>

### <span data-ttu-id="37d6f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="37d6f-149">System.String</span></span>

## <span data-ttu-id="37d6f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37d6f-150">OUTPUTS</span></span>

### <span data-ttu-id="37d6f-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="37d6f-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="37d6f-152">Note</span><span class="sxs-lookup"><span data-stu-id="37d6f-152">NOTES</span></span>

## <span data-ttu-id="37d6f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37d6f-153">RELATED LINKS</span></span>
