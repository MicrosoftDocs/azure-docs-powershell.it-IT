---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183839"
---
# <span data-ttu-id="814ea-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="814ea-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="814ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="814ea-102">SYNOPSIS</span></span>
<span data-ttu-id="814ea-103">Aggiorna (aggiorna server) le informazioni ricevute dal provider di servizi di ripristino siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="814ea-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="814ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="814ea-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="814ea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="814ea-105">DESCRIPTION</span></span>
<span data-ttu-id="814ea-106">Il cmdlet **Update-AzRecoveryServicesAsrServicesProvider** aggiorna le informazioni ricevute dal provider di servizi di ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="814ea-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="814ea-107">È possibile usare questo cmdlet per attivare un aggiornamento delle informazioni ricevute dal provider di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="814ea-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="814ea-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="814ea-108">EXAMPLES</span></span>

### <span data-ttu-id="814ea-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="814ea-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="814ea-110">Avvia l'operazione di aggiornamento delle informazioni dal provider di servizi ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="814ea-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="814ea-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="814ea-111">PARAMETERS</span></span>

### <span data-ttu-id="814ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814ea-112">-DefaultProfile</span></span>
<span data-ttu-id="814ea-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="814ea-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="814ea-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="814ea-114">-InputObject</span></span>
<span data-ttu-id="814ea-115">Specifica l'oggetto provider di servizi asr che identifica il server per cui aggiornare(aggiornare) le informazioni.</span><span class="sxs-lookup"><span data-stu-id="814ea-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="814ea-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="814ea-116">-Confirm</span></span>
<span data-ttu-id="814ea-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="814ea-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="814ea-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="814ea-118">-WhatIf</span></span>
<span data-ttu-id="814ea-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="814ea-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="814ea-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="814ea-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="814ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814ea-121">CommonParameters</span></span>
<span data-ttu-id="814ea-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="814ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814ea-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="814ea-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814ea-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="814ea-124">INPUTS</span></span>

### <span data-ttu-id="814ea-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="814ea-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="814ea-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="814ea-126">OUTPUTS</span></span>

### <span data-ttu-id="814ea-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="814ea-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="814ea-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="814ea-128">NOTES</span></span>

## <span data-ttu-id="814ea-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="814ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="814ea-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="814ea-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="814ea-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="814ea-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
