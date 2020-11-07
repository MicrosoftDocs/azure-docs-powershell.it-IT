---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 8e2b563563ca50e0fdf6913a9e9999e1a642ff9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687681"
---
# <span data-ttu-id="74165-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="74165-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="74165-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74165-102">SYNOPSIS</span></span>
<span data-ttu-id="74165-103">Ottiene le classificazioni dello spazio di archiviazione nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="74165-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74165-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74165-104">SYNTAX</span></span>

### <span data-ttu-id="74165-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="74165-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74165-106">ByName</span><span class="sxs-lookup"><span data-stu-id="74165-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74165-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="74165-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74165-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="74165-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74165-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="74165-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74165-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74165-110">DESCRIPTION</span></span>
<span data-ttu-id="74165-111">Il cmdlet **Get-AzureRmSiteRecoveryStorageClassification** ottiene le classificazioni di archiviazione nel ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="74165-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="74165-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74165-112">EXAMPLES</span></span>

## <span data-ttu-id="74165-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74165-113">PARAMETERS</span></span>

### <span data-ttu-id="74165-114">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="74165-114">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74165-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="74165-115">-FriendlyName</span></span>
<span data-ttu-id="74165-116">Specifica il nome descrittivo della classificazione di archiviazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74165-116">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74165-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="74165-117">-Name</span></span>
<span data-ttu-id="74165-118">Specifica il nome della classificazione di archiviazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74165-118">Specifies the name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74165-119">-Server</span><span class="sxs-lookup"><span data-stu-id="74165-119">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74165-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74165-120">-DefaultProfile</span></span>
<span data-ttu-id="74165-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74165-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74165-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74165-122">CommonParameters</span></span>
<span data-ttu-id="74165-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74165-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74165-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74165-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74165-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74165-125">INPUTS</span></span>

### <span data-ttu-id="74165-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="74165-126">ASRFabric</span></span>
<span data-ttu-id="74165-127">Il parametro "tessuto" accetta il valore di tipo "ASRFabric" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="74165-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="74165-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="74165-128">ASRServer</span></span>
<span data-ttu-id="74165-129">Il parametro ' server ' accetta il valore di tipo ' ASRServer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="74165-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="74165-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74165-130">OUTPUTS</span></span>

### <span data-ttu-id="74165-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="74165-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="74165-132">Note</span><span class="sxs-lookup"><span data-stu-id="74165-132">NOTES</span></span>

## <span data-ttu-id="74165-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74165-133">RELATED LINKS</span></span>

