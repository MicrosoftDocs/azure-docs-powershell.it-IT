---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5220271538903206876dd8d5c476824e1ac10874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521549"
---
# <span data-ttu-id="e30fa-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e30fa-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="e30fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e30fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e30fa-103">Elimina/Annulla la registrazione del provider di servizi di ripristino del ripristino di Azure sito specificato dall'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e30fa-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e30fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e30fa-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e30fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e30fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e30fa-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrServicesProvider** rimuove il provider di servizi di ripristino del ripristino di Azure sito specificato dal Vault.</span><span class="sxs-lookup"><span data-stu-id="e30fa-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="e30fa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e30fa-107">EXAMPLES</span></span>

### <span data-ttu-id="e30fa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e30fa-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="e30fa-109">Avvia l'eliminazione/annullamento della registrazione del provider di servizi di ripristino di Azure del sito specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e30fa-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e30fa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e30fa-110">PARAMETERS</span></span>

### <span data-ttu-id="e30fa-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e30fa-111">-Force</span></span>
<span data-ttu-id="e30fa-112">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="e30fa-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30fa-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e30fa-113">-InputObject</span></span>
<span data-ttu-id="e30fa-114">Oggetto di input per il cmdlet: l'oggetto provider servizi di ripristino ASR che corrisponde al provider di servizi di ripristino ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e30fa-114">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e30fa-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e30fa-115">-Confirm</span></span>
<span data-ttu-id="e30fa-116">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="e30fa-116">Specify if confirmation is required.</span></span> <span data-ttu-id="e30fa-117">Impostare il valore del parametro Confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="e30fa-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="e30fa-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e30fa-118">-WhatIf</span></span>
<span data-ttu-id="e30fa-119">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e30fa-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="e30fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30fa-120">CommonParameters</span></span>
<span data-ttu-id="e30fa-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e30fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30fa-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30fa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30fa-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e30fa-123">INPUTS</span></span>

### <span data-ttu-id="e30fa-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e30fa-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="e30fa-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e30fa-125">OUTPUTS</span></span>

### <span data-ttu-id="e30fa-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e30fa-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e30fa-127">Note</span><span class="sxs-lookup"><span data-stu-id="e30fa-127">NOTES</span></span>

## <span data-ttu-id="e30fa-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e30fa-128">RELATED LINKS</span></span>

[<span data-ttu-id="e30fa-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e30fa-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="e30fa-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e30fa-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
