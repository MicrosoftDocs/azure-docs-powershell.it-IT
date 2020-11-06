---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8a7b36b67b0ec1721da36dfeba920b556892c5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520622"
---
# <span data-ttu-id="b8540-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b8540-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="b8540-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8540-102">SYNOPSIS</span></span>
<span data-ttu-id="b8540-103">Elimina il tessuto di ripristino del sito di Azure specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b8540-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8540-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8540-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8540-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8540-105">DESCRIPTION</span></span>
<span data-ttu-id="b8540-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrFabric** rimuove il tessuto di ripristino del sito di Azure specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b8540-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="b8540-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8540-107">EXAMPLES</span></span>

### <span data-ttu-id="b8540-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b8540-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="b8540-109">Avvia l'eliminazione di tessuto specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b8540-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b8540-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8540-110">PARAMETERS</span></span>

### <span data-ttu-id="b8540-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8540-111">-DefaultProfile</span></span>
<span data-ttu-id="b8540-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8540-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8540-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b8540-113">-Force</span></span>
<span data-ttu-id="b8540-114">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="b8540-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="b8540-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8540-115">-InputObject</span></span>
<span data-ttu-id="b8540-116">L'oggetto di input per il cmdlet: l'oggetto tessuto ASR corrispondente al tessuto da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b8540-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8540-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b8540-117">-Confirm</span></span>
<span data-ttu-id="b8540-118">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="b8540-118">Specify if confirmation is required.</span></span> <span data-ttu-id="b8540-119">Impostare il valore del parametro Confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="b8540-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="b8540-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8540-120">-WhatIf</span></span>
<span data-ttu-id="b8540-121">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8540-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="b8540-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8540-122">CommonParameters</span></span>
<span data-ttu-id="b8540-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8540-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8540-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8540-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8540-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8540-125">INPUTS</span></span>

### <span data-ttu-id="b8540-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b8540-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b8540-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8540-127">OUTPUTS</span></span>

### <span data-ttu-id="b8540-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b8540-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b8540-129">Note</span><span class="sxs-lookup"><span data-stu-id="b8540-129">NOTES</span></span>

## <span data-ttu-id="b8540-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8540-130">RELATED LINKS</span></span>

[<span data-ttu-id="b8540-131">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b8540-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="b8540-132">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b8540-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
