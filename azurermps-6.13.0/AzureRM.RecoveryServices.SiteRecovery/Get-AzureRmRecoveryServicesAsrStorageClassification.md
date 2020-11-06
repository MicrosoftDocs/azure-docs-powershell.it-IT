---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: dc6e0cba8103884fc36413c0a2980892411852ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509195"
---
# <span data-ttu-id="285e0-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="285e0-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="285e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="285e0-102">SYNOPSIS</span></span>
<span data-ttu-id="285e0-103">Ottiene le classificazioni di archiviazione ASR disponibili nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="285e0-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="285e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="285e0-104">SYNTAX</span></span>

### <span data-ttu-id="285e0-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="285e0-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="285e0-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="285e0-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="285e0-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="285e0-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="285e0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="285e0-108">DESCRIPTION</span></span>
<span data-ttu-id="285e0-109">Il cmdlet Get-AzureRmRecoveryServicesAsrStorageClassification ottiene i dettagli delle classificazioni di archiviazione ASR **rilevate** nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="285e0-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="285e0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="285e0-110">EXAMPLES</span></span>

### <span data-ttu-id="285e0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="285e0-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="285e0-112">Elencare le classificazioni dello spazio di archiviazione individuate corrispondenti al tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="285e0-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="285e0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="285e0-113">PARAMETERS</span></span>

### <span data-ttu-id="285e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285e0-114">-DefaultProfile</span></span>
<span data-ttu-id="285e0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="285e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="285e0-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="285e0-116">-Fabric</span></span>
<span data-ttu-id="285e0-117">Specifica un oggetto tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="285e0-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="285e0-118">Il cmdlet ottiene i dettagli delle classificazioni dello spazio di archiviazione individuate corrispondenti al tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="285e0-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="285e0-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="285e0-119">-FriendlyName</span></span>
<span data-ttu-id="285e0-120">Specifica il nome descrittivo dell'oggetto di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="285e0-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="285e0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="285e0-121">-Name</span></span>
<span data-ttu-id="285e0-122">Specifica il nome dell'oggetto di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="285e0-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="285e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285e0-123">CommonParameters</span></span>
<span data-ttu-id="285e0-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285e0-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285e0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285e0-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="285e0-126">INPUTS</span></span>

### <span data-ttu-id="285e0-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="285e0-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="285e0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="285e0-128">OUTPUTS</span></span>

### <span data-ttu-id="285e0-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="285e0-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="285e0-130">Note</span><span class="sxs-lookup"><span data-stu-id="285e0-130">NOTES</span></span>

## <span data-ttu-id="285e0-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="285e0-131">RELATED LINKS</span></span>
