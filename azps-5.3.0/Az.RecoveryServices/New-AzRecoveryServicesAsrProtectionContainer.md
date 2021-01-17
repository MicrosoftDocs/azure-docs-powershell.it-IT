---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: fecc6f1911a82b20d3f96643ceed83486727f29f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474690"
---
# <span data-ttu-id="5e935-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5e935-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="5e935-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e935-102">SYNOPSIS</span></span>
<span data-ttu-id="5e935-103">Crea un contenitore di protezione per il ripristino di un sito Azure all'interno del tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="5e935-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="5e935-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e935-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e935-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e935-105">DESCRIPTION</span></span>
<span data-ttu-id="5e935-106">Il cmdlet New-AzRecoveryServicesAsrProtectionContainer crea un contenitore di protezione sotto il tessuto di recupero del sito Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="5e935-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="5e935-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e935-107">EXAMPLES</span></span>

### <span data-ttu-id="5e935-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e935-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="5e935-109">Avvia la creazione del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5e935-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5e935-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e935-110">PARAMETERS</span></span>

### <span data-ttu-id="5e935-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e935-111">-DefaultProfile</span></span>
<span data-ttu-id="5e935-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e935-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e935-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e935-113">-InputObject</span></span>
<span data-ttu-id="5e935-114">Crea il contenitore di protezione della replica nell'oggetto di input specificato (tessuto Azure).</span><span class="sxs-lookup"><span data-stu-id="5e935-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="5e935-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e935-115">-Name</span></span>
<span data-ttu-id="5e935-116">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="5e935-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="5e935-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e935-117">-Confirm</span></span>
<span data-ttu-id="5e935-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e935-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e935-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e935-119">-WhatIf</span></span>
<span data-ttu-id="5e935-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e935-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e935-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e935-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e935-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e935-122">CommonParameters</span></span>
<span data-ttu-id="5e935-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e935-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e935-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e935-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e935-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e935-125">INPUTS</span></span>

### <span data-ttu-id="5e935-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5e935-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5e935-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e935-127">OUTPUTS</span></span>

### <span data-ttu-id="5e935-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5e935-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e935-129">Note</span><span class="sxs-lookup"><span data-stu-id="5e935-129">NOTES</span></span>

## <span data-ttu-id="5e935-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e935-130">RELATED LINKS</span></span>
