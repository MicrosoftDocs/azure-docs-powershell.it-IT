---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 851978fafa35d36923adf4dd2c2a6e071c054d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687444"
---
# <span data-ttu-id="fb675-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="fb675-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="fb675-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb675-102">SYNOPSIS</span></span>
<span data-ttu-id="fb675-103">Ottiene un elenco di entità protettive o protette nella volta corrente del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="fb675-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb675-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb675-104">SYNTAX</span></span>

### <span data-ttu-id="fb675-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb675-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb675-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fb675-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb675-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fb675-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb675-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb675-108">DESCRIPTION</span></span>
<span data-ttu-id="fb675-109">Il cmdlet **Get-AzureRmSiteRecoveryProtectionEntity** ottiene un elenco di entità protetti o protette, ad esempio macchine virtuali, nell'attuale archivio di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="fb675-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="fb675-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb675-110">EXAMPLES</span></span>

## <span data-ttu-id="fb675-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb675-111">PARAMETERS</span></span>

### <span data-ttu-id="fb675-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb675-112">-DefaultProfile</span></span>
<span data-ttu-id="fb675-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb675-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb675-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fb675-114">-FriendlyName</span></span>
<span data-ttu-id="fb675-115">Specifica il nome descrittivo dell'entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="fb675-115">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb675-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb675-116">-Name</span></span>
<span data-ttu-id="fb675-117">Specifica il nome dell'entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="fb675-117">Specifies the name of the protection entity.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb675-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fb675-118">-ProtectionContainer</span></span>
<span data-ttu-id="fb675-119">Specifica l'oggetto contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="fb675-119">Specifies the protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb675-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb675-120">CommonParameters</span></span>
<span data-ttu-id="fb675-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb675-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb675-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb675-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb675-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb675-123">INPUTS</span></span>

### <span data-ttu-id="fb675-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fb675-124">ASRProtectionContainer</span></span>
<span data-ttu-id="fb675-125">Il parametro ' ProtectionContainer ' accetta il valore di tipo ' ASRProtectionContainer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fb675-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="fb675-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb675-126">OUTPUTS</span></span>

### <span data-ttu-id="fb675-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="fb675-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="fb675-128">Note</span><span class="sxs-lookup"><span data-stu-id="fb675-128">NOTES</span></span>

## <span data-ttu-id="fb675-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb675-129">RELATED LINKS</span></span>

[<span data-ttu-id="fb675-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="fb675-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
