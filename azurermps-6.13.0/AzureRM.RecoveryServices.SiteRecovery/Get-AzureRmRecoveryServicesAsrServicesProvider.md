---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 506009ac15fa1c9eeeb3e0b7ae902e3c42d1d468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687590"
---
# <span data-ttu-id="17ca3-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="17ca3-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="17ca3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="17ca3-103">Ottiene i dettagli dei provider di servizi di ripristino ASR registrati nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="17ca3-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17ca3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17ca3-104">SYNTAX</span></span>

### <span data-ttu-id="17ca3-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17ca3-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17ca3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="17ca3-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17ca3-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="17ca3-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17ca3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17ca3-108">DESCRIPTION</span></span>
<span data-ttu-id="17ca3-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrServicesProvider** ottiene le informazioni sui provider di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="17ca3-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="17ca3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17ca3-110">EXAMPLES</span></span>

### <span data-ttu-id="17ca3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17ca3-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="17ca3-112">Elenca tutti i provider di servizi di replica ASR registrati nel Vault di servizi di ripristino che corrispondono al tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="17ca3-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="17ca3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17ca3-113">PARAMETERS</span></span>

### <span data-ttu-id="17ca3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ca3-114">-DefaultProfile</span></span>
<span data-ttu-id="17ca3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17ca3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="17ca3-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="17ca3-116">-Fabric</span></span>
<span data-ttu-id="17ca3-117">Specifica l'oggetto del tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="17ca3-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17ca3-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="17ca3-118">-FriendlyName</span></span>
<span data-ttu-id="17ca3-119">Specifica il nome descrittivo del provider di servizi di ripristino ASR per ottenere informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="17ca3-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="17ca3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="17ca3-120">-Name</span></span>
<span data-ttu-id="17ca3-121">Specifica il nome del provider di servizi di ripristino ASR per cui ottenere i dettagli.</span><span class="sxs-lookup"><span data-stu-id="17ca3-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="17ca3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ca3-122">CommonParameters</span></span>
<span data-ttu-id="17ca3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17ca3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ca3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17ca3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ca3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17ca3-125">INPUTS</span></span>

### <span data-ttu-id="17ca3-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="17ca3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="17ca3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17ca3-127">OUTPUTS</span></span>

### <span data-ttu-id="17ca3-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="17ca3-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="17ca3-129">Note</span><span class="sxs-lookup"><span data-stu-id="17ca3-129">NOTES</span></span>

## <span data-ttu-id="17ca3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17ca3-130">RELATED LINKS</span></span>

[<span data-ttu-id="17ca3-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="17ca3-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="17ca3-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="17ca3-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
