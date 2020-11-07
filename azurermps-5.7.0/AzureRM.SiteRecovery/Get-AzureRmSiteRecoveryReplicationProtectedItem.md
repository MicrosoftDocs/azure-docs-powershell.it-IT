---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 210b8ca6d8165049edc190e24e4a435046e1461e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687442"
---
# <span data-ttu-id="d5369-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5369-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="d5369-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5369-102">SYNOPSIS</span></span>
<span data-ttu-id="d5369-103">Ottiene le proprietà degli elementi protetti per il ripristino di siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="d5369-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5369-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5369-104">SYNTAX</span></span>

### <span data-ttu-id="d5369-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d5369-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5369-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d5369-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5369-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d5369-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5369-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="d5369-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5369-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5369-109">DESCRIPTION</span></span>
<span data-ttu-id="d5369-110">Il cmdlet **Get-AzureRmSiteRecoveryReplicationProtectedItem** ottiene le proprietà degli elementi protetti per il ripristino di siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="d5369-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="d5369-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5369-111">EXAMPLES</span></span>

## <span data-ttu-id="d5369-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5369-112">PARAMETERS</span></span>

### <span data-ttu-id="d5369-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5369-113">-DefaultProfile</span></span>
<span data-ttu-id="d5369-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5369-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5369-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d5369-115">-FriendlyName</span></span>
<span data-ttu-id="d5369-116">Specifica il nome descrittivo dell'elemento protetto dalla replica ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5369-116">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5369-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5369-117">-Name</span></span>
<span data-ttu-id="d5369-118">Specifica il nome dell'elemento protetto dalla replica ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5369-118">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5369-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d5369-119">-ProtectableItem</span></span>
<span data-ttu-id="d5369-120">Specifica l'elemento protettivo corrispondente all'elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="d5369-120">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5369-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d5369-121">-ProtectionContainer</span></span>
<span data-ttu-id="d5369-122">Specifica l'oggetto contenitore di protezione per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="d5369-122">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5369-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5369-123">CommonParameters</span></span>
<span data-ttu-id="d5369-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5369-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5369-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5369-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5369-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5369-126">INPUTS</span></span>

### <span data-ttu-id="d5369-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d5369-127">ASRProtectableItem</span></span>
<span data-ttu-id="d5369-128">Il parametro ' ProtectableItem ' accetta il valore di tipo ' ASRProtectableItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d5369-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="d5369-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d5369-129">ASRProtectionContainer</span></span>
<span data-ttu-id="d5369-130">Il parametro ' ProtectionContainer ' accetta il valore di tipo ' ASRProtectionContainer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d5369-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="d5369-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5369-131">OUTPUTS</span></span>

### <span data-ttu-id="d5369-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d5369-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d5369-133">Note</span><span class="sxs-lookup"><span data-stu-id="d5369-133">NOTES</span></span>

## <span data-ttu-id="d5369-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5369-134">RELATED LINKS</span></span>

[<span data-ttu-id="d5369-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5369-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="d5369-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5369-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="d5369-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d5369-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
