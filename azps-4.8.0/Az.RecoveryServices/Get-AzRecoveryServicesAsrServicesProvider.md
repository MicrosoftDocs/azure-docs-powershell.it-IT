---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5ede0387f5aabb1a4f4c4814f8090e0feeda2bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189433"
---
# <span data-ttu-id="a6f56-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a6f56-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="a6f56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6f56-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f56-103">Ottiene i dettagli dei provider di servizi di ripristino ASR registrati nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a6f56-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="a6f56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6f56-104">SYNTAX</span></span>

### <span data-ttu-id="a6f56-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6f56-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6f56-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a6f56-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6f56-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a6f56-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6f56-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6f56-108">DESCRIPTION</span></span>
<span data-ttu-id="a6f56-109">Il cmdlet **Get-AzRecoveryServicesAsrServicesProvider** ottiene le informazioni sui provider di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="a6f56-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="a6f56-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6f56-110">EXAMPLES</span></span>

### <span data-ttu-id="a6f56-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6f56-111">Example 1</span></span>
```powershell
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="a6f56-112">Elenca tutti i provider di servizi di replica ASR registrati nel Vault di servizi di ripristino che corrispondono al tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="a6f56-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

### <span data-ttu-id="a6f56-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a6f56-113">Example 2</span></span>

<span data-ttu-id="a6f56-114">Ottiene i dettagli dei provider di servizi di ripristino ASR registrati nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a6f56-114">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span> <span data-ttu-id="a6f56-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a6f56-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrServicesProvider -Fabric $Fabric
```

## <span data-ttu-id="a6f56-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6f56-116">PARAMETERS</span></span>

### <span data-ttu-id="a6f56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f56-117">-DefaultProfile</span></span>
<span data-ttu-id="a6f56-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6f56-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a6f56-119">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="a6f56-119">-Fabric</span></span>
<span data-ttu-id="a6f56-120">Specifica l'oggetto del tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="a6f56-120">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="a6f56-121">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a6f56-121">-FriendlyName</span></span>
<span data-ttu-id="a6f56-122">Specifica il nome descrittivo del provider di servizi di ripristino ASR per ottenere informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="a6f56-122">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="a6f56-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6f56-123">-Name</span></span>
<span data-ttu-id="a6f56-124">Specifica il nome del provider di servizi di ripristino ASR per cui ottenere i dettagli.</span><span class="sxs-lookup"><span data-stu-id="a6f56-124">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="a6f56-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f56-125">CommonParameters</span></span>
<span data-ttu-id="a6f56-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f56-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f56-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6f56-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f56-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6f56-128">INPUTS</span></span>

### <span data-ttu-id="a6f56-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a6f56-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a6f56-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6f56-130">OUTPUTS</span></span>

### <span data-ttu-id="a6f56-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a6f56-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="a6f56-132">Note</span><span class="sxs-lookup"><span data-stu-id="a6f56-132">NOTES</span></span>

## <span data-ttu-id="a6f56-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6f56-133">RELATED LINKS</span></span>

[<span data-ttu-id="a6f56-134">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a6f56-134">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="a6f56-135">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a6f56-135">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)