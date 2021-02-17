---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: fecc6f1911a82b20d3f96643ceed83486727f29f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186615"
---
# <span data-ttu-id="424d0-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="424d0-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="424d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424d0-102">SYNOPSIS</span></span>
<span data-ttu-id="424d0-103">Crea un contenitore di Azure Site Recovery Protection all'interno del tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="424d0-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="424d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="424d0-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424d0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="424d0-105">DESCRIPTION</span></span>
<span data-ttu-id="424d0-106">Il cmdlet New-AzRecoveryServicesAsrProtectionContainer crea un contenitore di protezione nell'infrastruttura di azure site recovery specificata.</span><span class="sxs-lookup"><span data-stu-id="424d0-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="424d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="424d0-107">EXAMPLES</span></span>

### <span data-ttu-id="424d0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="424d0-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="424d0-109">Avvia la creazione del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="424d0-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="424d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="424d0-110">PARAMETERS</span></span>

### <span data-ttu-id="424d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424d0-111">-DefaultProfile</span></span>
<span data-ttu-id="424d0-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="424d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424d0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="424d0-113">-InputObject</span></span>
<span data-ttu-id="424d0-114">Crea il contenitore di protezione dalla replica nell'oggetto di input specificato (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="424d0-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="424d0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="424d0-115">-Name</span></span>
<span data-ttu-id="424d0-116">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="424d0-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="424d0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="424d0-117">-Confirm</span></span>
<span data-ttu-id="424d0-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424d0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424d0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424d0-119">-WhatIf</span></span>
<span data-ttu-id="424d0-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="424d0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="424d0-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="424d0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424d0-122">CommonParameters</span></span>
<span data-ttu-id="424d0-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424d0-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="424d0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424d0-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="424d0-125">INPUTS</span></span>

### <span data-ttu-id="424d0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="424d0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="424d0-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="424d0-127">OUTPUTS</span></span>

### <span data-ttu-id="424d0-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="424d0-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="424d0-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="424d0-129">NOTES</span></span>

## <span data-ttu-id="424d0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="424d0-130">RELATED LINKS</span></span>
