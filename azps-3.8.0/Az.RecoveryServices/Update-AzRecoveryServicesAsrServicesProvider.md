---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021471"
---
# <span data-ttu-id="bae70-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="bae70-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="bae70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bae70-102">SYNOPSIS</span></span>
<span data-ttu-id="bae70-103">Aggiorna (aggiornare il server) le informazioni ricevute dal provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="bae70-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="bae70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bae70-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bae70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bae70-105">DESCRIPTION</span></span>
<span data-ttu-id="bae70-106">Il cmdlet **Update-AzRecoveryServicesAsrServicesProvider** aggiorna le informazioni ricevute dal provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="bae70-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="bae70-107">Puoi usare questo cmdlet per attivare un aggiornamento delle informazioni ricevute dal provider di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bae70-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="bae70-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bae70-108">EXAMPLES</span></span>

### <span data-ttu-id="bae70-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bae70-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="bae70-110">Avvia l'operazione di aggiornamento delle informazioni dal provider di servizi ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bae70-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bae70-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bae70-111">PARAMETERS</span></span>

### <span data-ttu-id="bae70-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bae70-112">-DefaultProfile</span></span>
<span data-ttu-id="bae70-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bae70-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bae70-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bae70-114">-InputObject</span></span>
<span data-ttu-id="bae70-115">Specifica l'oggetto provider di servizi ASR che identifica il server per cui sono aggiornate le informazioni (aggiornata).</span><span class="sxs-lookup"><span data-stu-id="bae70-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bae70-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bae70-116">-Confirm</span></span>
<span data-ttu-id="bae70-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bae70-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bae70-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bae70-118">-WhatIf</span></span>
<span data-ttu-id="bae70-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bae70-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bae70-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bae70-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bae70-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bae70-121">CommonParameters</span></span>
<span data-ttu-id="bae70-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bae70-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bae70-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bae70-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bae70-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bae70-124">INPUTS</span></span>

### <span data-ttu-id="bae70-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="bae70-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="bae70-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bae70-126">OUTPUTS</span></span>

### <span data-ttu-id="bae70-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bae70-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bae70-128">Note</span><span class="sxs-lookup"><span data-stu-id="bae70-128">NOTES</span></span>

## <span data-ttu-id="bae70-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bae70-129">RELATED LINKS</span></span>

[<span data-ttu-id="bae70-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="bae70-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="bae70-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="bae70-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
