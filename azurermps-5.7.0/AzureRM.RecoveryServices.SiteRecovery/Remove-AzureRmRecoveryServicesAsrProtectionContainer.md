---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 496eeed8b4ed4b41ce2c67d47fc636711cd5cb84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514231"
---
# <span data-ttu-id="856b2-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="856b2-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="856b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="856b2-102">SYNOPSIS</span></span>
<span data-ttu-id="856b2-103">Elimina il contenitore di protezione specificato dal relativo tessuto.</span><span class="sxs-lookup"><span data-stu-id="856b2-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="856b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="856b2-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="856b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="856b2-105">DESCRIPTION</span></span>
<span data-ttu-id="856b2-106">Il cmdlet Remove-AzureRmRecoveryServicesAsrProtectionContainer Elimina il contenitore di protezione del ripristino di Azure site specificato.</span><span class="sxs-lookup"><span data-stu-id="856b2-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="856b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="856b2-107">EXAMPLES</span></span>

### <span data-ttu-id="856b2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="856b2-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="856b2-109">Avvia l'eliminazione del contenitore di protezione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione di rimozione.</span><span class="sxs-lookup"><span data-stu-id="856b2-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="856b2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="856b2-110">PARAMETERS</span></span>

### <span data-ttu-id="856b2-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="856b2-111">-Confirm</span></span>
<span data-ttu-id="856b2-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="856b2-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="856b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856b2-113">-DefaultProfile</span></span>
<span data-ttu-id="856b2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="856b2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="856b2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="856b2-115">-InputObject</span></span>
<span data-ttu-id="856b2-116">Specifica il contenitore di protezione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="856b2-116">Specifies the protection container to be removed .</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="856b2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="856b2-117">-WhatIf</span></span>
<span data-ttu-id="856b2-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="856b2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="856b2-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="856b2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="856b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856b2-120">CommonParameters</span></span>
<span data-ttu-id="856b2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856b2-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="856b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856b2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="856b2-123">INPUTS</span></span>

### <span data-ttu-id="856b2-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="856b2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="856b2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="856b2-125">OUTPUTS</span></span>

### <span data-ttu-id="856b2-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="856b2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="856b2-127">Note</span><span class="sxs-lookup"><span data-stu-id="856b2-127">NOTES</span></span>

## <span data-ttu-id="856b2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="856b2-128">RELATED LINKS</span></span>