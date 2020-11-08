---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: dc9f7dfa26b350a5dadea4bfa3afb9ad832fa063
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019637"
---
# <span data-ttu-id="71f28-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="71f28-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="71f28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71f28-102">SYNOPSIS</span></span>
<span data-ttu-id="71f28-103">Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="71f28-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="71f28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71f28-104">SYNTAX</span></span>

### <span data-ttu-id="71f28-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="71f28-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71f28-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="71f28-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71f28-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="71f28-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71f28-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="71f28-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71f28-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71f28-109">DESCRIPTION</span></span>
<span data-ttu-id="71f28-110">Usare **Remove-AzServiceFabricClientCertificate** per rimuovere un certificato client o i nomi di oggetto del certificato da usare per l'autenticazione del client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="71f28-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="71f28-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71f28-111">EXAMPLES</span></span>

### <span data-ttu-id="71f28-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="71f28-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="71f28-113">Questo comando rimuoverà il certificato client con l'identificazione personale "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" dal cluster.</span><span class="sxs-lookup"><span data-stu-id="71f28-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="71f28-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71f28-114">PARAMETERS</span></span>

### <span data-ttu-id="71f28-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="71f28-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="71f28-116">Specificare l'identificazione personale del certificato client che contiene solo le autorizzazioni di amministratore</span><span class="sxs-lookup"><span data-stu-id="71f28-116">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71f28-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="71f28-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="71f28-118">Specificare il nome comune del client, l'identificazione personale dell'autorità emittente e il tipo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="71f28-118">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71f28-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="71f28-119">-CommonName</span></span>
<span data-ttu-id="71f28-120">Specificare il nome comune del certificato client</span><span class="sxs-lookup"><span data-stu-id="71f28-120">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71f28-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f28-121">-DefaultProfile</span></span>
<span data-ttu-id="71f28-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71f28-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71f28-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="71f28-123">-IssuerThumbprint</span></span>
<span data-ttu-id="71f28-124">Specificare l'identificazione personale dell'autorità emittente del certificato client</span><span class="sxs-lookup"><span data-stu-id="71f28-124">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71f28-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="71f28-125">-Name</span></span>
<span data-ttu-id="71f28-126">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="71f28-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="71f28-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="71f28-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="71f28-128">Specificare l'identificazione personale del certificato client che ha solo l'autorizzazione di sola lettura</span><span class="sxs-lookup"><span data-stu-id="71f28-128">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71f28-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f28-129">-ResourceGroupName</span></span>
<span data-ttu-id="71f28-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71f28-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="71f28-131">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="71f28-131">-Thumbprint</span></span>
<span data-ttu-id="71f28-132">Specificare l'identificazione personale del certificato client</span><span class="sxs-lookup"><span data-stu-id="71f28-132">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71f28-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71f28-133">-Confirm</span></span>
<span data-ttu-id="71f28-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71f28-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71f28-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71f28-135">-WhatIf</span></span>
<span data-ttu-id="71f28-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71f28-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71f28-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71f28-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71f28-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f28-138">CommonParameters</span></span>
<span data-ttu-id="71f28-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f28-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f28-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71f28-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f28-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71f28-141">INPUTS</span></span>

### <span data-ttu-id="71f28-142">System. String</span><span class="sxs-lookup"><span data-stu-id="71f28-142">System.String</span></span>

### <span data-ttu-id="71f28-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="71f28-143">System.String[]</span></span>

### <span data-ttu-id="71f28-144">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="71f28-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="71f28-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71f28-145">OUTPUTS</span></span>

### <span data-ttu-id="71f28-146">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="71f28-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="71f28-147">Note</span><span class="sxs-lookup"><span data-stu-id="71f28-147">NOTES</span></span>

## <span data-ttu-id="71f28-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71f28-148">RELATED LINKS</span></span>

[<span data-ttu-id="71f28-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="71f28-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
