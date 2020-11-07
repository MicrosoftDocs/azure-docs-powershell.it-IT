---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 008c2b669ffdef61bb0745522f3a5d31775a99d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854026"
---
# <span data-ttu-id="f4c4f-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f4c4f-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="f4c4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c4f-103">Rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="f4c4f-103">Removes a log profile.</span></span>

## <span data-ttu-id="f4c4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4c4f-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4c4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="f4c4f-106">Il cmdlet **Remove-AzLogProfile** rimuove un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="f4c4f-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="f4c4f-107">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4c4f-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f4c4f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4c4f-108">EXAMPLES</span></span>

## <span data-ttu-id="f4c4f-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4c4f-109">PARAMETERS</span></span>

### <span data-ttu-id="f4c4f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c4f-110">-DefaultProfile</span></span>
<span data-ttu-id="f4c4f-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f4c4f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4c4f-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4c4f-112">-Name</span></span>
<span data-ttu-id="f4c4f-113">Specifica il nome del profilo del log da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f4c4f-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="f4c4f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4c4f-114">-PassThru</span></span>
<span data-ttu-id="f4c4f-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f4c4f-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f4c4f-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4c4f-116">-Confirm</span></span>
<span data-ttu-id="f4c4f-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c4f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c4f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c4f-118">-WhatIf</span></span>
<span data-ttu-id="f4c4f-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4c4f-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4c4f-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4c4f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c4f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c4f-121">CommonParameters</span></span>
<span data-ttu-id="f4c4f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4c4f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c4f-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4c4f-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c4f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4c4f-124">INPUTS</span></span>

### <span data-ttu-id="f4c4f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f4c4f-125">System.String</span></span>

## <span data-ttu-id="f4c4f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4c4f-126">OUTPUTS</span></span>

### <span data-ttu-id="f4c4f-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f4c4f-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="f4c4f-128">Note</span><span class="sxs-lookup"><span data-stu-id="f4c4f-128">NOTES</span></span>

## <span data-ttu-id="f4c4f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4c4f-129">RELATED LINKS</span></span>

[<span data-ttu-id="f4c4f-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f4c4f-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="f4c4f-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f4c4f-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


