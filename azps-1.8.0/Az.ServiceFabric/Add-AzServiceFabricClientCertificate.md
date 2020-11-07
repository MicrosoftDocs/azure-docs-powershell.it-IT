---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: bb6280eb623f52256eda5324e3d7980894fc91e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677086"
---
# <span data-ttu-id="a882b-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a882b-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="a882b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a882b-102">SYNOPSIS</span></span>
<span data-ttu-id="a882b-103">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="a882b-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="a882b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a882b-104">SYNTAX</span></span>

### <span data-ttu-id="a882b-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a882b-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a882b-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a882b-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a882b-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a882b-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a882b-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a882b-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a882b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a882b-109">DESCRIPTION</span></span>
<span data-ttu-id="a882b-110">USA **Add-AzServiceFabricClientCertificate** per aggiungere un nome comune e un'identificazione personale dell'autorità di certificazione o certificato al cluster, in modo che il client possa usarlo per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a882b-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="a882b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a882b-111">EXAMPLES</span></span>

### <span data-ttu-id="a882b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a882b-112">Example 1</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="a882b-113">Questo comando aggiungerà il certificato con l'identificazione personale "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" al cluster, in modo che il client possa usare il certificato come amministratore per comunicare con il cluster.</span><span class="sxs-lookup"><span data-stu-id="a882b-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="a882b-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a882b-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a882b-115">Questo comando aggiungerà un certificato client di sola lettura il cui nome comune è "Contoso.com" e l'identificazione personale dell'autorità di certificazione è "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" per il cluster.</span><span class="sxs-lookup"><span data-stu-id="a882b-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="a882b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a882b-116">PARAMETERS</span></span>

### <span data-ttu-id="a882b-117">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="a882b-117">-Admin</span></span>
<span data-ttu-id="a882b-118">Tipo di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="a882b-118">Client authentication type.</span></span>

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

### <span data-ttu-id="a882b-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a882b-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="a882b-120">Specificare l'identificazione personale del certificato client che contiene solo le autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a882b-120">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="a882b-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a882b-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="a882b-122">Specificare il nome comune del client, l'identificazione personale dell'autorità di emissione e il tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a882b-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="a882b-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a882b-123">-CommonName</span></span>
<span data-ttu-id="a882b-124">Specificare il nome comune del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a882b-124">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="a882b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a882b-125">-DefaultProfile</span></span>
<span data-ttu-id="a882b-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a882b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a882b-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a882b-127">-IssuerThumbprint</span></span>
<span data-ttu-id="a882b-128">Specificare l'identificazione personale dell'autorità emittente del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a882b-128">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="a882b-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="a882b-129">-Name</span></span>
<span data-ttu-id="a882b-130">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a882b-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a882b-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a882b-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="a882b-132">Specificare l'identificazione personale del certificato client con l'autorizzazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a882b-132">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="a882b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a882b-133">-ResourceGroupName</span></span>
<span data-ttu-id="a882b-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a882b-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a882b-135">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="a882b-135">-Thumbprint</span></span>
<span data-ttu-id="a882b-136">Specificare l'identificazione personale del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a882b-136">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="a882b-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a882b-137">-Confirm</span></span>
<span data-ttu-id="a882b-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a882b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a882b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a882b-139">-WhatIf</span></span>
<span data-ttu-id="a882b-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a882b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a882b-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a882b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a882b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a882b-142">CommonParameters</span></span>
<span data-ttu-id="a882b-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a882b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a882b-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a882b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a882b-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a882b-145">INPUTS</span></span>

### <span data-ttu-id="a882b-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a882b-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a882b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a882b-147">System.String</span></span>

### <span data-ttu-id="a882b-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="a882b-148">System.String[]</span></span>

### <span data-ttu-id="a882b-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="a882b-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="a882b-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a882b-150">OUTPUTS</span></span>

### <span data-ttu-id="a882b-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a882b-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a882b-152">Note</span><span class="sxs-lookup"><span data-stu-id="a882b-152">NOTES</span></span>

## <span data-ttu-id="a882b-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a882b-153">RELATED LINKS</span></span>

[<span data-ttu-id="a882b-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a882b-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
