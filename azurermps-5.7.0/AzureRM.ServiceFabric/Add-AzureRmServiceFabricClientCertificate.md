---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: c7b6e00ccbe368267fd6b110490df4f70b2229a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519359"
---
# <span data-ttu-id="a60cf-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a60cf-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="a60cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a60cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a60cf-103">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="a60cf-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a60cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a60cf-104">SYNTAX</span></span>

### <span data-ttu-id="a60cf-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a60cf-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60cf-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a60cf-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60cf-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a60cf-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a60cf-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a60cf-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a60cf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a60cf-109">DESCRIPTION</span></span>
<span data-ttu-id="a60cf-110">USA **Add-AzureRmServiceFabricClientCertificate** per aggiungere un nome comune e un'identificazione personale dell'autorità di certificazione o certificato al cluster, in modo che il client possa usarlo per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a60cf-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="a60cf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a60cf-111">EXAMPLES</span></span>

### <span data-ttu-id="a60cf-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a60cf-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="a60cf-113">Questo comando aggiungerà il certificato con l'identificazione personale "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" al cluster, in modo che il client possa usare il certificato come amministratore per comunicare con il cluster.</span><span class="sxs-lookup"><span data-stu-id="a60cf-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="a60cf-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a60cf-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a60cf-115">Questo comando aggiungerà un certificato client di sola lettura il cui nome comune è "Contoso.com" e l'identificazione personale dell'autorità di certificazione è "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" per il cluster.</span><span class="sxs-lookup"><span data-stu-id="a60cf-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="a60cf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a60cf-116">PARAMETERS</span></span>

### <span data-ttu-id="a60cf-117">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="a60cf-117">-Admin</span></span>
<span data-ttu-id="a60cf-118">Tipo di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="a60cf-118">Client authentication type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a60cf-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="a60cf-120">Specificare l'identificazione personale del certificato client che contiene solo le autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a60cf-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a60cf-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="a60cf-122">Specificare il nome comune del client, l'identificazione personale dell'autorità di emissione e il tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a60cf-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a60cf-123">-CommonName</span></span>
<span data-ttu-id="a60cf-124">Specificare il nome comune del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a60cf-124">Specify client certificate common name.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60cf-125">-DefaultProfile</span></span>
<span data-ttu-id="a60cf-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a60cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a60cf-127">-IssuerThumbprint</span></span>
<span data-ttu-id="a60cf-128">Specificare l'identificazione personale dell'autorità emittente del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a60cf-128">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="a60cf-129">-Name</span></span>
<span data-ttu-id="a60cf-130">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a60cf-130">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a60cf-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="a60cf-132">Specificare l'identificazione personale del certificato client con l'autorizzazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a60cf-132">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60cf-133">-ResourceGroupName</span></span>
<span data-ttu-id="a60cf-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a60cf-134">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-135">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="a60cf-135">-Thumbprint</span></span>
<span data-ttu-id="a60cf-136">Specificare l'identificazione personale del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a60cf-136">Specify client certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a60cf-137">-Confirm</span></span>
<span data-ttu-id="a60cf-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60cf-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60cf-139">-WhatIf</span></span>
<span data-ttu-id="a60cf-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a60cf-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a60cf-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a60cf-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60cf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60cf-142">CommonParameters</span></span>
<span data-ttu-id="a60cf-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60cf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60cf-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a60cf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60cf-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a60cf-145">INPUTS</span></span>

### <span data-ttu-id="a60cf-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a60cf-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="a60cf-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a60cf-147">System.String</span></span>

<span data-ttu-id="a60cf-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a60cf-148">System.Boolean</span></span>

## <span data-ttu-id="a60cf-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a60cf-149">OUTPUTS</span></span>

### <span data-ttu-id="a60cf-150">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="a60cf-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="a60cf-151">Note</span><span class="sxs-lookup"><span data-stu-id="a60cf-151">NOTES</span></span>

## <span data-ttu-id="a60cf-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a60cf-152">RELATED LINKS</span></span>

[<span data-ttu-id="a60cf-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a60cf-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
