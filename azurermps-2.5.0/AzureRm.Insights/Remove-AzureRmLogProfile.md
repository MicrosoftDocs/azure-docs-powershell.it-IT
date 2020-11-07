---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 78d2bff42382564bb07f680b5db8db39707ffb97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865824"
---
# <span data-ttu-id="0ceb5-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="0ceb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ceb5-102">SYNOPSIS</span></span>
<span data-ttu-id="0ceb5-103">Rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ceb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ceb5-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ceb5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ceb5-105">DESCRIPTION</span></span>
<span data-ttu-id="0ceb5-106">Il cmdlet **Remove-AzureRmLogProfile** rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="0ceb5-107">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0ceb5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ceb5-108">EXAMPLES</span></span>

## <span data-ttu-id="0ceb5-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ceb5-109">PARAMETERS</span></span>

### <span data-ttu-id="0ceb5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-110">-DefaultProfile</span></span>
<span data-ttu-id="0ceb5-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0ceb5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ceb5-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ceb5-112">-Name</span></span>
<span data-ttu-id="0ceb5-113">Specifica il nome del profilo del log da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ceb5-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ceb5-114">-PassThru</span></span>
<span data-ttu-id="0ceb5-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0ceb5-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0ceb5-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ceb5-116">-Confirm</span></span>
<span data-ttu-id="0ceb5-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ceb5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ceb5-118">-WhatIf</span></span>
<span data-ttu-id="0ceb5-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ceb5-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ceb5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ceb5-121">CommonParameters</span></span>
<span data-ttu-id="0ceb5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ceb5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ceb5-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ceb5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ceb5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ceb5-124">INPUTS</span></span>

### <span data-ttu-id="0ceb5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0ceb5-125">System.String</span></span>

## <span data-ttu-id="0ceb5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ceb5-126">OUTPUTS</span></span>

### <span data-ttu-id="0ceb5-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0ceb5-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0ceb5-128">Note</span><span class="sxs-lookup"><span data-stu-id="0ceb5-128">NOTES</span></span>

## <span data-ttu-id="0ceb5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ceb5-129">RELATED LINKS</span></span>

[<span data-ttu-id="0ceb5-130">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="0ceb5-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0ceb5-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


