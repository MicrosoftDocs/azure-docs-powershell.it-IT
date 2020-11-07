---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7a2508669c0beba7fc9edd92ac645ce149633e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686308"
---
# <span data-ttu-id="97cdc-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97cdc-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="97cdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="97cdc-103">Elimina il mapping del contenitore di protezione del ripristino di Azure site specificato.</span><span class="sxs-lookup"><span data-stu-id="97cdc-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97cdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97cdc-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97cdc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="97cdc-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** Elimina il mapping del contenitore di protezione del ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="97cdc-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="97cdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97cdc-107">EXAMPLES</span></span>

### <span data-ttu-id="97cdc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97cdc-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="97cdc-109">Avvia l'eliminazione del mapping del contenitore di protezione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="97cdc-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="97cdc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97cdc-110">PARAMETERS</span></span>

### <span data-ttu-id="97cdc-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97cdc-111">-Confirm</span></span>
<span data-ttu-id="97cdc-112">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="97cdc-112">Specify if confirmation is required.</span></span> <span data-ttu-id="97cdc-113">Impostare il valore del parametro Confirm su $false per ignorare la conferma</span><span class="sxs-lookup"><span data-stu-id="97cdc-113">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="97cdc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97cdc-114">-DefaultProfile</span></span>
<span data-ttu-id="97cdc-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97cdc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="97cdc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="97cdc-116">-Force</span></span>
<span data-ttu-id="97cdc-117">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="97cdc-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="97cdc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97cdc-118">-InputObject</span></span>
<span data-ttu-id="97cdc-119">Oggetto di input per il cmdlet: oggetto mapping del contenitore di protezione ASR corrispondente al contenitore di protezione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="97cdc-119">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97cdc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97cdc-120">-WhatIf</span></span>
<span data-ttu-id="97cdc-121">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97cdc-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="97cdc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97cdc-122">CommonParameters</span></span>
<span data-ttu-id="97cdc-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97cdc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97cdc-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97cdc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97cdc-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97cdc-125">INPUTS</span></span>

### <span data-ttu-id="97cdc-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97cdc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="97cdc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97cdc-127">OUTPUTS</span></span>

### <span data-ttu-id="97cdc-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="97cdc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="97cdc-129">Note</span><span class="sxs-lookup"><span data-stu-id="97cdc-129">NOTES</span></span>

## <span data-ttu-id="97cdc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97cdc-130">RELATED LINKS</span></span>

[<span data-ttu-id="97cdc-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97cdc-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="97cdc-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="97cdc-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
