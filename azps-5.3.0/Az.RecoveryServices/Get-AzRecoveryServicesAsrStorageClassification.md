---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476731"
---
# <span data-ttu-id="2538b-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2538b-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="2538b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2538b-102">SYNOPSIS</span></span>
<span data-ttu-id="2538b-103">Ottiene le classificazioni di archiviazione ASR disponibili nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2538b-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2538b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2538b-104">SYNTAX</span></span>

### <span data-ttu-id="2538b-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2538b-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2538b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2538b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2538b-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2538b-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2538b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2538b-108">DESCRIPTION</span></span>
<span data-ttu-id="2538b-109">Il cmdlet Get-AzRecoveryServicesAsrStorageClassification ottiene i dettagli delle classificazioni di archiviazione ASR **rilevate** nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2538b-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="2538b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2538b-110">EXAMPLES</span></span>

### <span data-ttu-id="2538b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2538b-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="2538b-112">Elencare le classificazioni dello spazio di archiviazione individuate corrispondenti al tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="2538b-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="2538b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2538b-113">PARAMETERS</span></span>

### <span data-ttu-id="2538b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2538b-114">-DefaultProfile</span></span>
<span data-ttu-id="2538b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2538b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2538b-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="2538b-116">-Fabric</span></span>
<span data-ttu-id="2538b-117">Specifica un oggetto tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="2538b-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="2538b-118">Il cmdlet ottiene i dettagli delle classificazioni dello spazio di archiviazione individuate corrispondenti al tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="2538b-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="2538b-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2538b-119">-FriendlyName</span></span>
<span data-ttu-id="2538b-120">Specifica il nome descrittivo dell'oggetto di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="2538b-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2538b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2538b-121">-Name</span></span>
<span data-ttu-id="2538b-122">Specifica il nome dell'oggetto di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="2538b-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="2538b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2538b-123">CommonParameters</span></span>
<span data-ttu-id="2538b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2538b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2538b-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2538b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2538b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2538b-126">INPUTS</span></span>

### <span data-ttu-id="2538b-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2538b-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2538b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2538b-128">OUTPUTS</span></span>

### <span data-ttu-id="2538b-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2538b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2538b-130">Note</span><span class="sxs-lookup"><span data-stu-id="2538b-130">NOTES</span></span>

## <span data-ttu-id="2538b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2538b-131">RELATED LINKS</span></span>
