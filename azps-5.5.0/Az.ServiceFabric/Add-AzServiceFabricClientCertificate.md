---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198663"
---
# <span data-ttu-id="6a2f3-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6a2f3-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="6a2f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2f3-103">Aggiungere il nome comune o l'immagine thumbprint al cluster ai fini dell'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="6a2f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a2f3-104">SYNTAX</span></span>

### <span data-ttu-id="6a2f3-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="6a2f3-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a2f3-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="6a2f3-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a2f3-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="6a2f3-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a2f3-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="6a2f3-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a2f3-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6a2f3-109">DESCRIPTION</span></span>
<span data-ttu-id="6a2f3-110">Usare **Add-AzServiceFabricClientCertificate** per aggiungere un nome comune e l'identificazione digitale dell'autorità di certificazione o del certificato al cluster, in modo che il client possa usarla per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="6a2f3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a2f3-111">EXAMPLES</span></span>

### <span data-ttu-id="6a2f3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a2f3-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="6a2f3-113">Questo comando aggiunge il certificato con immagine thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' al cluster, in modo che il client possa usare il certificato come amministratore per comunicare con il cluster.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="6a2f3-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6a2f3-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="6a2f3-115">Questo comando aggiunge al cluster un certificato client di sola lettura il cui nome comune è "Contoso.com" e l'emittente è "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A".</span><span class="sxs-lookup"><span data-stu-id="6a2f3-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="6a2f3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a2f3-116">PARAMETERS</span></span>

### <span data-ttu-id="6a2f3-117">-Admin</span><span class="sxs-lookup"><span data-stu-id="6a2f3-117">-Admin</span></span>
<span data-ttu-id="6a2f3-118">Tipo di autenticazione client</span><span class="sxs-lookup"><span data-stu-id="6a2f3-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2f3-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="6a2f3-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="6a2f3-120">Specificare l'immagine thumbprint del certificato client con autorizzazioni di amministratore</span><span class="sxs-lookup"><span data-stu-id="6a2f3-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="6a2f3-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="6a2f3-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="6a2f3-122">Specificare il nome comune del client, l'impronta digitale dell'autorità emittente e il tipo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="6a2f3-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="6a2f3-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="6a2f3-123">-CommonName</span></span>
<span data-ttu-id="6a2f3-124">Specificare il nome comune del certificato client</span><span class="sxs-lookup"><span data-stu-id="6a2f3-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="6a2f3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2f3-125">-DefaultProfile</span></span>
<span data-ttu-id="6a2f3-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a2f3-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="6a2f3-127">-IssuerThumbprint</span></span>
<span data-ttu-id="6a2f3-128">Specificare l'immagine thumbprint dell'autorità di certificazione client</span><span class="sxs-lookup"><span data-stu-id="6a2f3-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="6a2f3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6a2f3-129">-Name</span></span>
<span data-ttu-id="6a2f3-130">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="6a2f3-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="6a2f3-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="6a2f3-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="6a2f3-132">Specificare l'immagine thumbprint del certificato client con autorizzazione di sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a2f3-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="6a2f3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a2f3-133">-ResourceGroupName</span></span>
<span data-ttu-id="6a2f3-134">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6a2f3-135">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="6a2f3-135">-Thumbprint</span></span>
<span data-ttu-id="6a2f3-136">Specificare l'impronta digitale del certificato client</span><span class="sxs-lookup"><span data-stu-id="6a2f3-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="6a2f3-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a2f3-137">-Confirm</span></span>
<span data-ttu-id="6a2f3-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a2f3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a2f3-139">-WhatIf</span></span>
<span data-ttu-id="6a2f3-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a2f3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a2f3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2f3-142">CommonParameters</span></span>
<span data-ttu-id="6a2f3-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2f3-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a2f3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2f3-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="6a2f3-145">INPUTS</span></span>

### <span data-ttu-id="6a2f3-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6a2f3-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6a2f3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6a2f3-147">System.String</span></span>

### <span data-ttu-id="6a2f3-148">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6a2f3-148">System.String[]</span></span>

### <span data-ttu-id="6a2f3-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="6a2f3-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="6a2f3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a2f3-150">OUTPUTS</span></span>

### <span data-ttu-id="6a2f3-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6a2f3-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6a2f3-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="6a2f3-152">NOTES</span></span>

## <span data-ttu-id="6a2f3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a2f3-153">RELATED LINKS</span></span>

[<span data-ttu-id="6a2f3-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6a2f3-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
