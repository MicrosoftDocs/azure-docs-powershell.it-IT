---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512587"
---
# <span data-ttu-id="2fba0-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2fba0-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="2fba0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fba0-102">SYNOPSIS</span></span>
<span data-ttu-id="2fba0-103">Rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="2fba0-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fba0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fba0-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fba0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fba0-105">DESCRIPTION</span></span>
<span data-ttu-id="2fba0-106">Il cmdlet **Remove-AzureRmLogProfile** rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="2fba0-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="2fba0-107">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2fba0-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2fba0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fba0-108">EXAMPLES</span></span>

## <span data-ttu-id="2fba0-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fba0-109">PARAMETERS</span></span>

### <span data-ttu-id="2fba0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fba0-110">-DefaultProfile</span></span>
<span data-ttu-id="2fba0-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2fba0-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fba0-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fba0-112">-Name</span></span>
<span data-ttu-id="2fba0-113">Specifica il nome del profilo del log da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2fba0-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fba0-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fba0-114">-PassThru</span></span>
<span data-ttu-id="2fba0-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2fba0-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2fba0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fba0-116">CommonParameters</span></span>
<span data-ttu-id="2fba0-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fba0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fba0-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fba0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fba0-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fba0-119">INPUTS</span></span>

### <span data-ttu-id="2fba0-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2fba0-120">None</span></span>
<span data-ttu-id="2fba0-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2fba0-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fba0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fba0-122">OUTPUTS</span></span>

### <span data-ttu-id="2fba0-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2fba0-123">AzureOperationResponse</span></span>

## <span data-ttu-id="2fba0-124">Note</span><span class="sxs-lookup"><span data-stu-id="2fba0-124">NOTES</span></span>

## <span data-ttu-id="2fba0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fba0-125">RELATED LINKS</span></span>

[<span data-ttu-id="2fba0-126">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2fba0-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="2fba0-127">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2fba0-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


