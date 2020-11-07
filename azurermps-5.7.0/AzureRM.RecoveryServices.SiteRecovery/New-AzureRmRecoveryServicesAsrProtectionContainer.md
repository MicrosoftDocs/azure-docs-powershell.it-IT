---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 73d57e6e73b0e7e84dd3fb8bfff04ac8705bd108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687024"
---
# <span data-ttu-id="67341-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="67341-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="67341-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67341-102">SYNOPSIS</span></span>
<span data-ttu-id="67341-103">Crea un contenitore di protezione per il ripristino di un sito Azure all'interno del tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="67341-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67341-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67341-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67341-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67341-105">DESCRIPTION</span></span>
<span data-ttu-id="67341-106">Il cmdlet New-AzureRmRecoveryServicesAsrProtectionContainer crea un contenitore di protezione sotto il tessuto di recupero del sito Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="67341-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="67341-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67341-107">EXAMPLES</span></span>

### <span data-ttu-id="67341-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67341-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="67341-109">Avvia la creazione del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="67341-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="67341-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67341-110">PARAMETERS</span></span>

### <span data-ttu-id="67341-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67341-111">-Confirm</span></span>
<span data-ttu-id="67341-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67341-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67341-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67341-113">-DefaultProfile</span></span>
<span data-ttu-id="67341-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67341-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67341-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67341-115">-InputObject</span></span>
<span data-ttu-id="67341-116">Crea il contenitore di protezione della replica nell'oggetto di input specificato (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="67341-116">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67341-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="67341-117">-Name</span></span>
<span data-ttu-id="67341-118">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="67341-118">Name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67341-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67341-119">-WhatIf</span></span>
<span data-ttu-id="67341-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67341-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67341-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67341-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67341-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67341-122">CommonParameters</span></span>
<span data-ttu-id="67341-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67341-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67341-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67341-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67341-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67341-125">INPUTS</span></span>

### <span data-ttu-id="67341-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="67341-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="67341-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67341-127">OUTPUTS</span></span>

### <span data-ttu-id="67341-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="67341-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="67341-129">Note</span><span class="sxs-lookup"><span data-stu-id="67341-129">NOTES</span></span>

## <span data-ttu-id="67341-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67341-130">RELATED LINKS</span></span>
