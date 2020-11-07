---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687106"
---
# <span data-ttu-id="6654c-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6654c-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="6654c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6654c-102">SYNOPSIS</span></span>
<span data-ttu-id="6654c-103">Aggiorna (aggiornare il server) le informazioni ricevute dal provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="6654c-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6654c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6654c-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6654c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6654c-105">DESCRIPTION</span></span>
<span data-ttu-id="6654c-106">Il cmdlet **Update-AzureRmRecoveryServicesAsrServicesProvider** aggiorna le informazioni ricevute dal provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="6654c-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="6654c-107">Puoi usare questo cmdlet per attivare un aggiornamento delle informazioni ricevute dal provider di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6654c-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="6654c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6654c-108">EXAMPLES</span></span>

### <span data-ttu-id="6654c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6654c-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="6654c-110">Avvia l'operazione di aggiornamento delle informazioni dal provider di servizi ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6654c-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="6654c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6654c-111">PARAMETERS</span></span>

### <span data-ttu-id="6654c-112">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6654c-112">-InputObject</span></span>
<span data-ttu-id="6654c-113">Input Object: specifica l'oggetto provider di servizi ASR che corrisponde al provider di servizi ASR che identifica il server per cui le informazioni sono aggiornate (aggiornata).</span><span class="sxs-lookup"><span data-stu-id="6654c-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="6654c-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6654c-114">-Confirm</span></span>
<span data-ttu-id="6654c-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6654c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6654c-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6654c-116">-WhatIf</span></span>
<span data-ttu-id="6654c-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6654c-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6654c-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6654c-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6654c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6654c-119">CommonParameters</span></span>
<span data-ttu-id="6654c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6654c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6654c-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6654c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6654c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6654c-122">INPUTS</span></span>

### <span data-ttu-id="6654c-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6654c-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="6654c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6654c-124">OUTPUTS</span></span>

### <span data-ttu-id="6654c-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="6654c-125">System.Object</span></span>

## <span data-ttu-id="6654c-126">Note</span><span class="sxs-lookup"><span data-stu-id="6654c-126">NOTES</span></span>

## <span data-ttu-id="6654c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6654c-127">RELATED LINKS</span></span>

[<span data-ttu-id="6654c-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6654c-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="6654c-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6654c-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
