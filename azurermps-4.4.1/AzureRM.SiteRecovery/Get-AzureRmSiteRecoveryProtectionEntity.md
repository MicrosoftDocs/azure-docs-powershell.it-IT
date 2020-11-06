---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521524"
---
# <span data-ttu-id="64c8e-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="64c8e-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="64c8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="64c8e-103">Ottiene un elenco di entità protettive o protette nella volta corrente del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="64c8e-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64c8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64c8e-104">SYNTAX</span></span>

### <span data-ttu-id="64c8e-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64c8e-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c8e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="64c8e-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c8e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="64c8e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64c8e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64c8e-108">DESCRIPTION</span></span>
<span data-ttu-id="64c8e-109">Il cmdlet **Get-AzureRmSiteRecoveryProtectionEntity** ottiene un elenco di entità protetti o protette, ad esempio macchine virtuali, nell'attuale archivio di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="64c8e-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="64c8e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64c8e-110">EXAMPLES</span></span>

## <span data-ttu-id="64c8e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64c8e-111">PARAMETERS</span></span>

### <span data-ttu-id="64c8e-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="64c8e-112">-FriendlyName</span></span>
<span data-ttu-id="64c8e-113">Specifica il nome descrittivo dell'entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="64c8e-113">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c8e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="64c8e-114">-Name</span></span>
<span data-ttu-id="64c8e-115">Specifica il nome dell'entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="64c8e-115">Specifies the name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c8e-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="64c8e-116">-ProtectionContainer</span></span>
<span data-ttu-id="64c8e-117">Specifica l'oggetto contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="64c8e-117">Specifies the protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c8e-118">-DefaultProfile</span></span>
<span data-ttu-id="64c8e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64c8e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64c8e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c8e-120">CommonParameters</span></span>
<span data-ttu-id="64c8e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c8e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c8e-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c8e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c8e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64c8e-123">INPUTS</span></span>

### <span data-ttu-id="64c8e-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="64c8e-124">ASRProtectionContainer</span></span>
<span data-ttu-id="64c8e-125">Il parametro ' ProtectionContainer ' accetta il valore di tipo ' ASRProtectionContainer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="64c8e-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="64c8e-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64c8e-126">OUTPUTS</span></span>

### <span data-ttu-id="64c8e-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="64c8e-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="64c8e-128">Note</span><span class="sxs-lookup"><span data-stu-id="64c8e-128">NOTES</span></span>

## <span data-ttu-id="64c8e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64c8e-129">RELATED LINKS</span></span>

[<span data-ttu-id="64c8e-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="64c8e-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
