---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 9f0021658784c767e35d903a0a191ba28932f57a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677679"
---
# <span data-ttu-id="b07ea-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="b07ea-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="b07ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b07ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b07ea-103">Ottiene le classificazioni di archiviazione ASR disponibili nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b07ea-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="b07ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b07ea-104">SYNTAX</span></span>

### <span data-ttu-id="b07ea-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b07ea-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b07ea-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b07ea-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b07ea-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b07ea-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b07ea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b07ea-108">DESCRIPTION</span></span>
<span data-ttu-id="b07ea-109">Il cmdlet Get-AzRecoveryServicesAsrStorageClassification ottiene i dettagli delle classificazioni di archiviazione ASR **rilevate** nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b07ea-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="b07ea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b07ea-110">EXAMPLES</span></span>

### <span data-ttu-id="b07ea-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b07ea-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="b07ea-112">Elencare le classificazioni dello spazio di archiviazione individuate corrispondenti al tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="b07ea-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="b07ea-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b07ea-113">PARAMETERS</span></span>

### <span data-ttu-id="b07ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07ea-114">-DefaultProfile</span></span>
<span data-ttu-id="b07ea-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b07ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07ea-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="b07ea-116">-Fabric</span></span>
<span data-ttu-id="b07ea-117">Specifica un oggetto tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="b07ea-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="b07ea-118">Il cmdlet ottiene i dettagli delle classificazioni dello spazio di archiviazione individuate corrispondenti al tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="b07ea-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="b07ea-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b07ea-119">-FriendlyName</span></span>
<span data-ttu-id="b07ea-120">Specifica il nome descrittivo dell'oggetto di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b07ea-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="b07ea-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b07ea-121">-Name</span></span>
<span data-ttu-id="b07ea-122">Specifica il nome dell'oggetto di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b07ea-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="b07ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07ea-123">CommonParameters</span></span>
<span data-ttu-id="b07ea-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07ea-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07ea-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b07ea-126">INPUTS</span></span>

### <span data-ttu-id="b07ea-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b07ea-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b07ea-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b07ea-128">OUTPUTS</span></span>

### <span data-ttu-id="b07ea-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="b07ea-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="b07ea-130">Note</span><span class="sxs-lookup"><span data-stu-id="b07ea-130">NOTES</span></span>

## <span data-ttu-id="b07ea-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b07ea-131">RELATED LINKS</span></span>
