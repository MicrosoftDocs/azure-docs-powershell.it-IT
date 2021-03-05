---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 83dbf747e2ddcd001320ac746b7c505df73a8169
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970045"
---
# <span data-ttu-id="6d472-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6d472-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="6d472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d472-102">SYNOPSIS</span></span>
<span data-ttu-id="6d472-103">Aggiorna (aggiorna server) le informazioni ricevute dal provider di servizi di ripristino siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d472-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="6d472-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d472-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d472-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d472-105">DESCRIPTION</span></span>
<span data-ttu-id="6d472-106">Il cmdlet **Update-AzRecoveryServicesAsrServicesProvider** aggiorna le informazioni ricevute dal provider di servizi di ripristino dei siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d472-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="6d472-107">È possibile usare questo cmdlet per attivare un aggiornamento delle informazioni ricevute dal provider di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6d472-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="6d472-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d472-108">EXAMPLES</span></span>

### <span data-ttu-id="6d472-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d472-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="6d472-110">Avvia l'operazione di aggiornamento delle informazioni dal provider di servizi ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6d472-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6d472-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d472-111">PARAMETERS</span></span>

### <span data-ttu-id="6d472-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d472-112">-DefaultProfile</span></span>
<span data-ttu-id="6d472-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d472-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6d472-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d472-114">-InputObject</span></span>
<span data-ttu-id="6d472-115">Specifica l'oggetto provider di servizi ASR che identifica il server per cui aggiornare(aggiornare) le informazioni.</span><span class="sxs-lookup"><span data-stu-id="6d472-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="6d472-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d472-116">-Confirm</span></span>
<span data-ttu-id="6d472-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d472-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d472-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d472-118">-WhatIf</span></span>
<span data-ttu-id="6d472-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d472-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d472-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d472-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d472-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d472-121">CommonParameters</span></span>
<span data-ttu-id="6d472-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d472-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d472-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d472-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d472-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d472-124">INPUTS</span></span>

### <span data-ttu-id="6d472-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6d472-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="6d472-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d472-126">OUTPUTS</span></span>

### <span data-ttu-id="6d472-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6d472-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6d472-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d472-128">NOTES</span></span>

## <span data-ttu-id="6d472-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d472-129">RELATED LINKS</span></span>

[<span data-ttu-id="6d472-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6d472-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="6d472-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6d472-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
