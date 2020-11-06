---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 823ad4b0f7eff8f80fea012bdef4b3c2662d55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509668"
---
# <span data-ttu-id="51529-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51529-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="51529-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51529-102">SYNOPSIS</span></span>
<span data-ttu-id="51529-103">Aggiorna (aggiornare il server) le informazioni ricevute dal provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="51529-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51529-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51529-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51529-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51529-105">DESCRIPTION</span></span>
<span data-ttu-id="51529-106">Il cmdlet **Update-AzureRmRecoveryServicesAsrServicesProvider** aggiorna le informazioni ricevute dal provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="51529-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="51529-107">Puoi usare questo cmdlet per attivare un aggiornamento delle informazioni ricevute dal provider di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="51529-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="51529-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51529-108">EXAMPLES</span></span>

### <span data-ttu-id="51529-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51529-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="51529-110">Avvia l'operazione di aggiornamento delle informazioni dal provider di servizi ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="51529-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="51529-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51529-111">PARAMETERS</span></span>

### <span data-ttu-id="51529-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51529-112">-Confirm</span></span>
<span data-ttu-id="51529-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51529-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51529-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51529-114">-DefaultProfile</span></span>
<span data-ttu-id="51529-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51529-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="51529-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51529-116">-InputObject</span></span>
<span data-ttu-id="51529-117">Specifica l'oggetto provider di servizi ASR che identifica il server per cui sono aggiornate le informazioni (aggiornata).</span><span class="sxs-lookup"><span data-stu-id="51529-117">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="51529-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51529-118">-WhatIf</span></span>
<span data-ttu-id="51529-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51529-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51529-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51529-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51529-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51529-121">CommonParameters</span></span>
<span data-ttu-id="51529-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51529-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51529-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51529-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51529-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51529-124">INPUTS</span></span>

### <span data-ttu-id="51529-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51529-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="51529-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51529-126">OUTPUTS</span></span>

### <span data-ttu-id="51529-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="51529-127">System.Object</span></span>

## <span data-ttu-id="51529-128">Note</span><span class="sxs-lookup"><span data-stu-id="51529-128">NOTES</span></span>

## <span data-ttu-id="51529-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51529-129">RELATED LINKS</span></span>

[<span data-ttu-id="51529-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51529-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="51529-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51529-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
