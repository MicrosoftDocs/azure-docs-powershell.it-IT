---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198647"
---
# <span data-ttu-id="8e886-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8e886-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="8e886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e886-102">SYNOPSIS</span></span>
<span data-ttu-id="8e886-103">Rimuovere uno o più certificati client o i nomi degli oggetto del certificato usati per l'autenticazione client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="8e886-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="8e886-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e886-104">SYNTAX</span></span>

### <span data-ttu-id="8e886-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="8e886-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e886-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="8e886-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e886-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="8e886-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e886-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="8e886-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e886-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e886-109">DESCRIPTION</span></span>
<span data-ttu-id="8e886-110">Usare **Remove-AzServiceFabricClientCertificate** per rimuovere uno o più nomi di oggetto o certificato client da usare per l'autenticazione client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="8e886-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="8e886-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e886-111">EXAMPLES</span></span>

### <span data-ttu-id="8e886-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e886-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="8e886-113">Questo comando rimuove il certificato client con immagine thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' dal cluster.</span><span class="sxs-lookup"><span data-stu-id="8e886-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="8e886-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e886-114">PARAMETERS</span></span>

### <span data-ttu-id="8e886-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="8e886-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="8e886-116">Specificare l'immagine thumbprint del certificato client con autorizzazioni di amministratore</span><span class="sxs-lookup"><span data-stu-id="8e886-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="8e886-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="8e886-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="8e886-118">Specificare il nome comune del client, l'impronta digitale dell'autorità emittente e il tipo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="8e886-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="8e886-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="8e886-119">-CommonName</span></span>
<span data-ttu-id="8e886-120">Specificare il nome comune del certificato client</span><span class="sxs-lookup"><span data-stu-id="8e886-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="8e886-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e886-121">-DefaultProfile</span></span>
<span data-ttu-id="8e886-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e886-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e886-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="8e886-123">-IssuerThumbprint</span></span>
<span data-ttu-id="8e886-124">Specificare l'immagine thumbprint dell'autorità di certificazione client</span><span class="sxs-lookup"><span data-stu-id="8e886-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="8e886-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8e886-125">-Name</span></span>
<span data-ttu-id="8e886-126">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="8e886-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="8e886-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="8e886-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="8e886-128">Specificare l'immagine thumbprint del certificato client con autorizzazione di sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e886-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="8e886-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e886-129">-ResourceGroupName</span></span>
<span data-ttu-id="8e886-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e886-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8e886-131">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="8e886-131">-Thumbprint</span></span>
<span data-ttu-id="8e886-132">Specificare l'impronta digitale del certificato client</span><span class="sxs-lookup"><span data-stu-id="8e886-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="8e886-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e886-133">-Confirm</span></span>
<span data-ttu-id="8e886-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e886-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e886-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e886-135">-WhatIf</span></span>
<span data-ttu-id="8e886-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e886-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e886-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e886-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e886-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e886-138">CommonParameters</span></span>
<span data-ttu-id="8e886-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e886-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e886-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e886-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e886-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e886-141">INPUTS</span></span>

### <span data-ttu-id="8e886-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8e886-142">System.String</span></span>

### <span data-ttu-id="8e886-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8e886-143">System.String[]</span></span>

### <span data-ttu-id="8e886-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="8e886-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="8e886-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e886-145">OUTPUTS</span></span>

### <span data-ttu-id="8e886-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="8e886-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8e886-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e886-147">NOTES</span></span>

## <span data-ttu-id="8e886-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e886-148">RELATED LINKS</span></span>

[<span data-ttu-id="8e886-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="8e886-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
