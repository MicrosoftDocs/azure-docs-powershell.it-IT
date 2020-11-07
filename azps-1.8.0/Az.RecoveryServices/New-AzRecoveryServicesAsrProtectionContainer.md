---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 12c5132037e451681434620b65afd6e93235d65b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677618"
---
# <span data-ttu-id="327b1-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="327b1-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="327b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="327b1-102">SYNOPSIS</span></span>
<span data-ttu-id="327b1-103">Crea un contenitore di protezione per il ripristino di un sito Azure all'interno del tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="327b1-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="327b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="327b1-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="327b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="327b1-105">DESCRIPTION</span></span>
<span data-ttu-id="327b1-106">Il cmdlet New-AzRecoveryServicesAsrProtectionContainer crea un contenitore di protezione sotto il tessuto di recupero del sito Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="327b1-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="327b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="327b1-107">EXAMPLES</span></span>

### <span data-ttu-id="327b1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="327b1-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="327b1-109">Avvia la creazione del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="327b1-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="327b1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="327b1-110">PARAMETERS</span></span>

### <span data-ttu-id="327b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327b1-111">-DefaultProfile</span></span>
<span data-ttu-id="327b1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="327b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="327b1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="327b1-113">-InputObject</span></span>
<span data-ttu-id="327b1-114">Crea il contenitore di protezione della replica nell'oggetto di input specificato (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="327b1-114">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="327b1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="327b1-115">-Name</span></span>
<span data-ttu-id="327b1-116">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="327b1-116">Name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327b1-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="327b1-117">-Confirm</span></span>
<span data-ttu-id="327b1-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="327b1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327b1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="327b1-119">-WhatIf</span></span>
<span data-ttu-id="327b1-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="327b1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="327b1-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="327b1-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327b1-122">CommonParameters</span></span>
<span data-ttu-id="327b1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="327b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327b1-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="327b1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327b1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="327b1-125">INPUTS</span></span>

### <span data-ttu-id="327b1-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="327b1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="327b1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="327b1-127">OUTPUTS</span></span>

### <span data-ttu-id="327b1-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="327b1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="327b1-129">Note</span><span class="sxs-lookup"><span data-stu-id="327b1-129">NOTES</span></span>

## <span data-ttu-id="327b1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="327b1-130">RELATED LINKS</span></span>
