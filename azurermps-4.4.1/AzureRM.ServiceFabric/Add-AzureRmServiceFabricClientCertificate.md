---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: 37db0181ea135a0cdb00cddc0a18780fe9fe2d7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687684"
---
# <span data-ttu-id="e6a56-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e6a56-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="e6a56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6a56-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a56-103">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="e6a56-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6a56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6a56-104">SYNTAX</span></span>

### <span data-ttu-id="e6a56-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6a56-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a56-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e6a56-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a56-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e6a56-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a56-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6a56-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a56-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6a56-109">DESCRIPTION</span></span>
<span data-ttu-id="e6a56-110">USA **Add-AzureRmServiceFabricClientCertificate** per aggiungere un nome comune e un'identificazione personale dell'autorità di certificazione o certificato al cluster, in modo che il client possa usarlo per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e6a56-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="e6a56-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6a56-111">EXAMPLES</span></span>

### <span data-ttu-id="e6a56-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6a56-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -IsAdmin
```

<span data-ttu-id="e6a56-113">Questo comando aggiungerà il certificato con l'identificazione personale "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" al cluster, in modo che il client possa usare il certificato come amministratore per comunicare con il cluster.</span><span class="sxs-lookup"><span data-stu-id="e6a56-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="e6a56-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e6a56-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="e6a56-115">Questo comando aggiungerà un certificato client di sola lettura il cui nome comune è "Contoso.com" e l'identificazione personale dell'autorità di certificazione è "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" per il cluster.</span><span class="sxs-lookup"><span data-stu-id="e6a56-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="e6a56-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6a56-116">PARAMETERS</span></span>

### <span data-ttu-id="e6a56-117">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="e6a56-117">-Admin</span></span>
<span data-ttu-id="e6a56-118">Tipo di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="e6a56-118">Client authentication type.</span></span>

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

### <span data-ttu-id="e6a56-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6a56-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="e6a56-120">Specificare l'identificazione personale del certificato client che contiene solo le autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="e6a56-120">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="e6a56-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="e6a56-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="e6a56-122">Specificare il nome comune del client, l'identificazione personale dell'autorità di emissione e il tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e6a56-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="e6a56-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="e6a56-123">-CommonName</span></span>
<span data-ttu-id="e6a56-124">Specificare il nome comune del certificato client.</span><span class="sxs-lookup"><span data-stu-id="e6a56-124">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="e6a56-125">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6a56-125">-IssuerThumbprint</span></span>
<span data-ttu-id="e6a56-126">Specificare l'identificazione personale dell'autorità emittente del certificato client.</span><span class="sxs-lookup"><span data-stu-id="e6a56-126">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="e6a56-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6a56-127">-Name</span></span>
<span data-ttu-id="e6a56-128">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e6a56-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e6a56-129">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="e6a56-129">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="e6a56-130">Specificare l'identificazione personale del certificato client con l'autorizzazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e6a56-130">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="e6a56-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a56-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6a56-132">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e6a56-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e6a56-133">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="e6a56-133">-Thumbprint</span></span>
<span data-ttu-id="e6a56-134">Specificare l'identificazione personale del certificato client.</span><span class="sxs-lookup"><span data-stu-id="e6a56-134">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="e6a56-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6a56-135">-Confirm</span></span>
<span data-ttu-id="e6a56-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a56-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a56-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a56-137">-WhatIf</span></span>
<span data-ttu-id="e6a56-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6a56-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6a56-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6a56-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a56-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a56-140">-DefaultProfile</span></span>
<span data-ttu-id="e6a56-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a56-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6a56-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a56-142">CommonParameters</span></span>
<span data-ttu-id="e6a56-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a56-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a56-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a56-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a56-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6a56-145">INPUTS</span></span>

### <span data-ttu-id="e6a56-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6a56-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="e6a56-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a56-147">System.String</span></span>

<span data-ttu-id="e6a56-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6a56-148">System.Boolean</span></span>

## <span data-ttu-id="e6a56-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6a56-149">OUTPUTS</span></span>

### <span data-ttu-id="e6a56-150">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="e6a56-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="e6a56-151">Note</span><span class="sxs-lookup"><span data-stu-id="e6a56-151">NOTES</span></span>

## <span data-ttu-id="e6a56-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6a56-152">RELATED LINKS</span></span>

[<span data-ttu-id="e6a56-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e6a56-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
