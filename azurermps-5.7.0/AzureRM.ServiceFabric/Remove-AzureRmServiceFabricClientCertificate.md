---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: e508afc5ab66a3e2aec49131bf2c8bf0e9d31259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685815"
---
# <span data-ttu-id="a1e13-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a1e13-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="a1e13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1e13-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e13-103">Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="a1e13-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1e13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1e13-104">SYNTAX</span></span>

### <span data-ttu-id="a1e13-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a1e13-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e13-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a1e13-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e13-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="a1e13-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e13-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a1e13-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1e13-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1e13-109">DESCRIPTION</span></span>
<span data-ttu-id="a1e13-110">Usare **Remove-AzureRmServiceFabricClientCertificate** per rimuovere un certificato client o i nomi di oggetto del certificato da usare per l'autenticazione del client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="a1e13-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="a1e13-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1e13-111">EXAMPLES</span></span>

### <span data-ttu-id="a1e13-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1e13-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a1e13-113">Questo comando rimuoverà il certificato client con l'identificazione personale "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" dal cluster.</span><span class="sxs-lookup"><span data-stu-id="a1e13-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="a1e13-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1e13-114">PARAMETERS</span></span>

### <span data-ttu-id="a1e13-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a1e13-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="a1e13-116">Specificare l'identificazione personale del certificato client che contiene solo le autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a1e13-116">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="a1e13-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a1e13-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="a1e13-118">Specificare il nome comune del client, l'identificazione personale dell'autorità di emissione e il tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="a1e13-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="a1e13-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a1e13-119">-CommonName</span></span>
<span data-ttu-id="a1e13-120">Specificare il nome comune del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a1e13-120">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="a1e13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e13-121">-DefaultProfile</span></span>
<span data-ttu-id="a1e13-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e13-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1e13-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a1e13-123">-IssuerThumbprint</span></span>
<span data-ttu-id="a1e13-124">Specificare l'identificazione personale dell'autorità emittente del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a1e13-124">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="a1e13-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1e13-125">-Name</span></span>
<span data-ttu-id="a1e13-126">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a1e13-126">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a1e13-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="a1e13-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="a1e13-128">Specificare l'identificazione personale del certificato client con l'autorizzazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a1e13-128">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="a1e13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e13-129">-ResourceGroupName</span></span>
<span data-ttu-id="a1e13-130">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1e13-130">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a1e13-131">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="a1e13-131">-Thumbprint</span></span>
<span data-ttu-id="a1e13-132">Specificare l'identificazione personale del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a1e13-132">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="a1e13-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1e13-133">-Confirm</span></span>
<span data-ttu-id="a1e13-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1e13-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e13-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e13-135">-WhatIf</span></span>
<span data-ttu-id="a1e13-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1e13-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1e13-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1e13-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1e13-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e13-138">CommonParameters</span></span>
<span data-ttu-id="a1e13-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e13-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e13-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e13-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e13-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1e13-141">INPUTS</span></span>

### <span data-ttu-id="a1e13-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1e13-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="a1e13-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a1e13-143">System.String</span></span>

<span data-ttu-id="a1e13-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1e13-144">System.Boolean</span></span>

## <span data-ttu-id="a1e13-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1e13-145">OUTPUTS</span></span>

### <span data-ttu-id="a1e13-146">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="a1e13-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="a1e13-147">Note</span><span class="sxs-lookup"><span data-stu-id="a1e13-147">NOTES</span></span>

## <span data-ttu-id="a1e13-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1e13-148">RELATED LINKS</span></span>

[<span data-ttu-id="a1e13-149">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a1e13-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)