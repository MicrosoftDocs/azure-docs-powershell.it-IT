---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: d1bd4dc4a3fd47d19d76568e9c60a51f09d739c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514799"
---
# <span data-ttu-id="7a516-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7a516-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="7a516-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a516-102">SYNOPSIS</span></span>
<span data-ttu-id="7a516-103">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="7a516-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a516-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a516-104">SYNTAX</span></span>

### <span data-ttu-id="7a516-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="7a516-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a516-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="7a516-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a516-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="7a516-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a516-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="7a516-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a516-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a516-109">DESCRIPTION</span></span>
<span data-ttu-id="7a516-110">USA **Add-AzureRmServiceFabricClientCertificate** per aggiungere un nome comune e un'identificazione personale dell'autorità di certificazione o certificato al cluster, in modo che il client possa usarlo per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="7a516-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="7a516-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a516-111">EXAMPLES</span></span>

### <span data-ttu-id="7a516-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a516-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="7a516-113">Questo comando aggiungerà il certificato con l'identificazione personale "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" al cluster, in modo che il client possa usare il certificato come amministratore per comunicare con il cluster.</span><span class="sxs-lookup"><span data-stu-id="7a516-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="7a516-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7a516-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="7a516-115">Questo comando aggiungerà un certificato client di sola lettura il cui nome comune è "Contoso.com" e l'identificazione personale dell'autorità di certificazione è "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" per il cluster.</span><span class="sxs-lookup"><span data-stu-id="7a516-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="7a516-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a516-116">PARAMETERS</span></span>

### <span data-ttu-id="7a516-117">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="7a516-117">-Admin</span></span>
<span data-ttu-id="7a516-118">Tipo di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="7a516-118">Client authentication type.</span></span>

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

### <span data-ttu-id="7a516-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="7a516-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="7a516-120">Specificare l'identificazione personale del certificato client che contiene solo le autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="7a516-120">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="7a516-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="7a516-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="7a516-122">Specificare il nome comune del client, l'identificazione personale dell'autorità di emissione e il tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="7a516-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="7a516-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="7a516-123">-CommonName</span></span>
<span data-ttu-id="7a516-124">Specificare il nome comune del certificato client.</span><span class="sxs-lookup"><span data-stu-id="7a516-124">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="7a516-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a516-125">-DefaultProfile</span></span>
<span data-ttu-id="7a516-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a516-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a516-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="7a516-127">-IssuerThumbprint</span></span>
<span data-ttu-id="7a516-128">Specificare l'identificazione personale dell'autorità emittente del certificato client.</span><span class="sxs-lookup"><span data-stu-id="7a516-128">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="7a516-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a516-129">-Name</span></span>
<span data-ttu-id="7a516-130">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="7a516-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7a516-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="7a516-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="7a516-132">Specificare l'identificazione personale del certificato client con l'autorizzazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7a516-132">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="7a516-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a516-133">-ResourceGroupName</span></span>
<span data-ttu-id="7a516-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a516-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7a516-135">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="7a516-135">-Thumbprint</span></span>
<span data-ttu-id="7a516-136">Specificare l'identificazione personale del certificato client.</span><span class="sxs-lookup"><span data-stu-id="7a516-136">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="7a516-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a516-137">-Confirm</span></span>
<span data-ttu-id="7a516-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a516-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a516-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a516-139">-WhatIf</span></span>
<span data-ttu-id="7a516-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a516-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a516-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a516-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a516-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a516-142">CommonParameters</span></span>
<span data-ttu-id="7a516-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a516-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a516-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a516-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a516-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a516-145">INPUTS</span></span>

### <span data-ttu-id="7a516-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a516-146">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="7a516-147">Parametri: admin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a516-147">Parameters: Admin (ByValue)</span></span>

### <span data-ttu-id="7a516-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7a516-148">System.String</span></span>
<span data-ttu-id="7a516-149">Parameters: CommonName (ByValue), IssuerThumbprint (ByValue), identificazione digitale (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a516-149">Parameters: CommonName (ByValue), IssuerThumbprint (ByValue), Thumbprint (ByValue)</span></span>

### <span data-ttu-id="7a516-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="7a516-150">System.String[]</span></span>
<span data-ttu-id="7a516-151">Parametri: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a516-151">Parameters: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span></span>

### <span data-ttu-id="7a516-152">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="7a516-152">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>
<span data-ttu-id="7a516-153">Parametri: ClientCertificateCommonName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a516-153">Parameters: ClientCertificateCommonName (ByValue)</span></span>

## <span data-ttu-id="7a516-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a516-154">OUTPUTS</span></span>

### <span data-ttu-id="7a516-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="7a516-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7a516-156">Note</span><span class="sxs-lookup"><span data-stu-id="7a516-156">NOTES</span></span>

## <span data-ttu-id="7a516-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a516-157">RELATED LINKS</span></span>

[<span data-ttu-id="7a516-158">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7a516-158">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
