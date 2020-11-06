---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 2aa8855365ea74a00df875fb62bfec49a8c591ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514223"
---
# <span data-ttu-id="4d8cb-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4d8cb-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="4d8cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8cb-103">Elimina/Annulla la registrazione del provider di servizi di ripristino del ripristino di Azure sito specificato dall'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d8cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d8cb-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d8cb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d8cb-105">DESCRIPTION</span></span>
<span data-ttu-id="4d8cb-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrServicesProvider** rimuove il provider di servizi di ripristino del ripristino di Azure sito specificato dal Vault.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="4d8cb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d8cb-107">EXAMPLES</span></span>

### <span data-ttu-id="4d8cb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d8cb-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="4d8cb-109">Avvia l'eliminazione/annullamento della registrazione del provider di servizi di ripristino di Azure del sito specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4d8cb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d8cb-110">PARAMETERS</span></span>

### <span data-ttu-id="4d8cb-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d8cb-111">-Confirm</span></span>
<span data-ttu-id="4d8cb-112">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-112">Specify if confirmation is required.</span></span> <span data-ttu-id="4d8cb-113">Impostare il valore del parametro Confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="4d8cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8cb-114">-DefaultProfile</span></span>
<span data-ttu-id="4d8cb-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="4d8cb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4d8cb-116">-Force</span></span>
<span data-ttu-id="4d8cb-117">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="4d8cb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d8cb-118">-InputObject</span></span>
<span data-ttu-id="4d8cb-119">Oggetto di input per il cmdlet: l'oggetto provider servizi di ripristino ASR che corrisponde al provider di servizi di ripristino ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-119">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="4d8cb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d8cb-120">-WhatIf</span></span>
<span data-ttu-id="4d8cb-121">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="4d8cb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8cb-122">CommonParameters</span></span>
<span data-ttu-id="4d8cb-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d8cb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8cb-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d8cb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8cb-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d8cb-125">INPUTS</span></span>

### <span data-ttu-id="4d8cb-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4d8cb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="4d8cb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d8cb-127">OUTPUTS</span></span>

### <span data-ttu-id="4d8cb-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4d8cb-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4d8cb-129">Note</span><span class="sxs-lookup"><span data-stu-id="4d8cb-129">NOTES</span></span>

## <span data-ttu-id="4d8cb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d8cb-130">RELATED LINKS</span></span>

[<span data-ttu-id="4d8cb-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4d8cb-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="4d8cb-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4d8cb-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
