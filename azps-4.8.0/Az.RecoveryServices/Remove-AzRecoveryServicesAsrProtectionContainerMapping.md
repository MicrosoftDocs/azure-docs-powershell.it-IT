---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031535"
---
# <span data-ttu-id="ab3cc-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ab3cc-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="ab3cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3cc-103">Elimina il mapping del contenitore di protezione del ripristino di Azure site specificato.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="ab3cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab3cc-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab3cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="ab3cc-106">Il cmdlet **Remove-AzRecoveryServicesAsrProtectionContainerMapping** Elimina il mapping del contenitore di protezione del ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="ab3cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab3cc-107">EXAMPLES</span></span>

### <span data-ttu-id="ab3cc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab3cc-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="ab3cc-109">Avvia l'eliminazione del mapping del contenitore di protezione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ab3cc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab3cc-110">PARAMETERS</span></span>

### <span data-ttu-id="ab3cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3cc-111">-DefaultProfile</span></span>
<span data-ttu-id="ab3cc-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ab3cc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ab3cc-113">-Force</span></span>
<span data-ttu-id="ab3cc-114">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="ab3cc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab3cc-115">-InputObject</span></span>
<span data-ttu-id="ab3cc-116">Oggetto di input per il cmdlet: oggetto mapping del contenitore di protezione ASR corrispondente al contenitore di protezione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3cc-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab3cc-117">-Confirm</span></span>
<span data-ttu-id="ab3cc-118">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-118">Specify if confirmation is required.</span></span> <span data-ttu-id="ab3cc-119">Impostare il valore del parametro Confirm su $false per ignorare la conferma</span><span class="sxs-lookup"><span data-stu-id="ab3cc-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="ab3cc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab3cc-120">-WhatIf</span></span>
<span data-ttu-id="ab3cc-121">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="ab3cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3cc-122">CommonParameters</span></span>
<span data-ttu-id="ab3cc-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab3cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3cc-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab3cc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3cc-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab3cc-125">INPUTS</span></span>

### <span data-ttu-id="ab3cc-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ab3cc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="ab3cc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab3cc-127">OUTPUTS</span></span>

### <span data-ttu-id="ab3cc-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ab3cc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ab3cc-129">Note</span><span class="sxs-lookup"><span data-stu-id="ab3cc-129">NOTES</span></span>

## <span data-ttu-id="ab3cc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab3cc-130">RELATED LINKS</span></span>

[<span data-ttu-id="ab3cc-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ab3cc-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="ab3cc-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ab3cc-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
