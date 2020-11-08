---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190673"
---
# <span data-ttu-id="ea1a9-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ea1a9-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="ea1a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1a9-103">Elimina/Annulla la registrazione del provider di servizi di ripristino del ripristino di Azure sito specificato dall'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="ea1a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea1a9-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea1a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea1a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea1a9-106">Il cmdlet **Remove-AzRecoveryServicesAsrServicesProvider** rimuove il provider di servizi di ripristino del ripristino di Azure sito specificato dal Vault.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="ea1a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea1a9-107">EXAMPLES</span></span>

### <span data-ttu-id="ea1a9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea1a9-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="ea1a9-109">Avvia l'eliminazione/annullamento della registrazione del provider di servizi di ripristino di Azure del sito specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ea1a9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea1a9-110">PARAMETERS</span></span>

### <span data-ttu-id="ea1a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1a9-111">-DefaultProfile</span></span>
<span data-ttu-id="ea1a9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ea1a9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ea1a9-113">-Force</span></span>
<span data-ttu-id="ea1a9-114">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea1a9-115">-InputObject</span></span>
<span data-ttu-id="ea1a9-116">Oggetto di input per il cmdlet: l'oggetto provider servizi di ripristino ASR che corrisponde al provider di servizi di ripristino ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="ea1a9-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea1a9-117">-Confirm</span></span>
<span data-ttu-id="ea1a9-118">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-118">Specify if confirmation is required.</span></span> <span data-ttu-id="ea1a9-119">Impostare il valore del parametro Confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="ea1a9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1a9-120">-WhatIf</span></span>
<span data-ttu-id="ea1a9-121">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="ea1a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1a9-122">CommonParameters</span></span>
<span data-ttu-id="ea1a9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1a9-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea1a9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1a9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea1a9-125">INPUTS</span></span>

### <span data-ttu-id="ea1a9-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ea1a9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="ea1a9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea1a9-127">OUTPUTS</span></span>

### <span data-ttu-id="ea1a9-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea1a9-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea1a9-129">Note</span><span class="sxs-lookup"><span data-stu-id="ea1a9-129">NOTES</span></span>

## <span data-ttu-id="ea1a9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea1a9-130">RELATED LINKS</span></span>

[<span data-ttu-id="ea1a9-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ea1a9-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="ea1a9-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ea1a9-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
