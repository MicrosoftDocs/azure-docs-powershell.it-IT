---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: d5c2032828c5d34b94af8d448155c18b6d8b06c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687446"
---
# <span data-ttu-id="da8c2-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="da8c2-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="da8c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="da8c2-103">Ottiene i contenitori di protezione per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="da8c2-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da8c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da8c2-104">SYNTAX</span></span>

### <span data-ttu-id="da8c2-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da8c2-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da8c2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="da8c2-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da8c2-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="da8c2-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da8c2-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="da8c2-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da8c2-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="da8c2-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da8c2-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="da8c2-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da8c2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da8c2-111">DESCRIPTION</span></span>
<span data-ttu-id="da8c2-112">Il cmdlet **Get-AzureRmSiteRecoveryProtectionContainer** ottiene i contenitori di protezione per il Vault di ripristino del sito Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="da8c2-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="da8c2-113">Un contenitore di protezione è un contenitore logico per gli oggetti protetti, ad esempio le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="da8c2-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="da8c2-114">I criteri di protezione definiscono le impostazioni di replica per gli elementi protetti e possono essere associati a un contenitore di protezione e applicati a un'entità protetta.</span><span class="sxs-lookup"><span data-stu-id="da8c2-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="da8c2-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da8c2-115">EXAMPLES</span></span>

## <span data-ttu-id="da8c2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da8c2-116">PARAMETERS</span></span>

### <span data-ttu-id="da8c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8c2-117">-DefaultProfile</span></span>
<span data-ttu-id="da8c2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da8c2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da8c2-119">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="da8c2-119">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da8c2-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="da8c2-120">-FriendlyName</span></span>
<span data-ttu-id="da8c2-121">Specifica il nome descrittivo del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="da8c2-121">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da8c2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="da8c2-122">-Name</span></span>
<span data-ttu-id="da8c2-123">Specifica il nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="da8c2-123">Specifies the name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da8c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8c2-124">CommonParameters</span></span>
<span data-ttu-id="da8c2-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da8c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8c2-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da8c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8c2-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da8c2-127">INPUTS</span></span>

### <span data-ttu-id="da8c2-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="da8c2-128">ASRFabric</span></span>
<span data-ttu-id="da8c2-129">Il parametro "tessuto" accetta il valore di tipo "ASRFabric" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="da8c2-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="da8c2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da8c2-130">OUTPUTS</span></span>

### <span data-ttu-id="da8c2-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="da8c2-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="da8c2-132">Note</span><span class="sxs-lookup"><span data-stu-id="da8c2-132">NOTES</span></span>

## <span data-ttu-id="da8c2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da8c2-133">RELATED LINKS</span></span>

