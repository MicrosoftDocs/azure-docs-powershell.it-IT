---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 6ffd3a295ecc228ec395a00ba597f2d7b0967a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685973"
---
# <span data-ttu-id="6a565-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="6a565-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="6a565-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a565-102">SYNOPSIS</span></span>
<span data-ttu-id="6a565-103">Ottiene informazioni sulle reti gestite dal ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="6a565-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a565-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a565-104">SYNTAX</span></span>

### <span data-ttu-id="6a565-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a565-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a565-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="6a565-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a565-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="6a565-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a565-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="6a565-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a565-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="6a565-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a565-110">ByName</span><span class="sxs-lookup"><span data-stu-id="6a565-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a565-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6a565-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a565-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a565-112">DESCRIPTION</span></span>
<span data-ttu-id="6a565-113">Il cmdlet **Get-AzureRmSiteRecoveryNetwork** ottiene informazioni sulle reti di ripristino dei siti di Azure per l'attuale archivio di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="6a565-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6a565-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a565-114">EXAMPLES</span></span>

## <span data-ttu-id="6a565-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a565-115">PARAMETERS</span></span>

### <span data-ttu-id="6a565-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a565-116">-DefaultProfile</span></span>
<span data-ttu-id="6a565-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a565-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a565-118">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="6a565-118">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a565-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6a565-119">-FriendlyName</span></span>
<span data-ttu-id="6a565-120">Specifica il nome descrittivo della rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6a565-120">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a565-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a565-121">-Name</span></span>
<span data-ttu-id="6a565-122">Specifica il nome della rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6a565-122">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a565-123">-Server</span><span class="sxs-lookup"><span data-stu-id="6a565-123">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a565-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a565-124">CommonParameters</span></span>
<span data-ttu-id="6a565-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a565-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a565-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a565-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a565-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a565-127">INPUTS</span></span>

### <span data-ttu-id="6a565-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6a565-128">ASRFabric</span></span>
<span data-ttu-id="6a565-129">Il parametro "tessuto" accetta il valore di tipo "ASRFabric" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6a565-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="6a565-130">Stringa</span><span class="sxs-lookup"><span data-stu-id="6a565-130">String</span></span>
<span data-ttu-id="6a565-131">Il parametro "FriendlyName" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6a565-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6a565-132">Stringa</span><span class="sxs-lookup"><span data-stu-id="6a565-132">String</span></span>
<span data-ttu-id="6a565-133">Il parametro "FriendlyName" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6a565-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6a565-134">Stringa</span><span class="sxs-lookup"><span data-stu-id="6a565-134">String</span></span>
<span data-ttu-id="6a565-135">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6a565-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6a565-136">Stringa</span><span class="sxs-lookup"><span data-stu-id="6a565-136">String</span></span>
<span data-ttu-id="6a565-137">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6a565-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6a565-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="6a565-138">ASRServer</span></span>
<span data-ttu-id="6a565-139">Il parametro ' server ' accetta il valore di tipo ' ASRServer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6a565-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="6a565-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a565-140">OUTPUTS</span></span>

### <span data-ttu-id="6a565-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="6a565-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="6a565-142">Note</span><span class="sxs-lookup"><span data-stu-id="6a565-142">NOTES</span></span>

## <span data-ttu-id="6a565-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a565-143">RELATED LINKS</span></span>

