---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a51be31c510d7e428ced0c9ce5ab73a80ab28f75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509683"
---
# <span data-ttu-id="0b683-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0b683-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="0b683-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b683-102">SYNOPSIS</span></span>
<span data-ttu-id="0b683-103">Elimina il mapping di rete ASR specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0b683-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b683-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b683-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b683-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b683-105">DESCRIPTION</span></span>
<span data-ttu-id="0b683-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrNetworkMapping** Elimina il mapping di rete ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="0b683-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="0b683-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b683-107">EXAMPLES</span></span>

### <span data-ttu-id="0b683-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b683-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="0b683-109">Avvia l'eliminazione del mapping di rete ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0b683-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0b683-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b683-110">PARAMETERS</span></span>

### <span data-ttu-id="0b683-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b683-111">-Confirm</span></span>
<span data-ttu-id="0b683-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b683-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b683-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b683-113">-DefaultProfile</span></span>
<span data-ttu-id="0b683-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b683-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="0b683-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b683-115">-InputObject</span></span>
<span data-ttu-id="0b683-116">Oggetto di input per il cmdlet: l'oggetto mapping di rete ASR corrispondente al mapping di rete ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0b683-116">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b683-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b683-117">-WhatIf</span></span>
<span data-ttu-id="0b683-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b683-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b683-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b683-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b683-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b683-120">CommonParameters</span></span>
<span data-ttu-id="0b683-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b683-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b683-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b683-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b683-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b683-123">INPUTS</span></span>

### <span data-ttu-id="0b683-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0b683-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="0b683-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b683-125">OUTPUTS</span></span>

### <span data-ttu-id="0b683-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0b683-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0b683-127">Note</span><span class="sxs-lookup"><span data-stu-id="0b683-127">NOTES</span></span>

## <span data-ttu-id="0b683-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b683-128">RELATED LINKS</span></span>

[<span data-ttu-id="0b683-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0b683-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="0b683-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0b683-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
