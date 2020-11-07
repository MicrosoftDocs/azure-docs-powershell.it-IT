---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 76de3ad08e6acb0035cfa2a9ca5d353fcbf38033
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687734"
---
# <span data-ttu-id="2af0a-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2af0a-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="2af0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2af0a-102">SYNOPSIS</span></span>
<span data-ttu-id="2af0a-103">Rimuove un nodo DSC dalla gestione di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="2af0a-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2af0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2af0a-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2af0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2af0a-105">DESCRIPTION</span></span>
<span data-ttu-id="2af0a-106">Il cmdlet **Unregister-AzureRmAutomationDscNode** rimuove un nodo DSC (APS desired state Configuration) dalla gestione di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2af0a-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="2af0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2af0a-107">EXAMPLES</span></span>

### <span data-ttu-id="2af0a-108">Esempio 1: rimuovere un nodo Azure DSC dalla gestione di un account di automazione</span><span class="sxs-lookup"><span data-stu-id="2af0a-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="2af0a-109">Questo comando rimuove il nodo DSC che ha il GUID specificato dalla gestione dall'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2af0a-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="2af0a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2af0a-110">PARAMETERS</span></span>

### <span data-ttu-id="2af0a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2af0a-111">-AutomationAccountName</span></span>
<span data-ttu-id="2af0a-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="2af0a-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af0a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2af0a-113">-Force</span></span>
<span data-ttu-id="2af0a-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="2af0a-114">ps_force</span></span>

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

### <span data-ttu-id="2af0a-115">-ID</span><span class="sxs-lookup"><span data-stu-id="2af0a-115">-Id</span></span>
<span data-ttu-id="2af0a-116">Specifica l'ID univoco del nodo DSC rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2af0a-116">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af0a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2af0a-117">-ResourceGroupName</span></span>
<span data-ttu-id="2af0a-118">Specifica il nome di un gruppo di risorse in cui questo cmdlet Annulla la registrazione di un nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="2af0a-118">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af0a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2af0a-119">-Confirm</span></span>
<span data-ttu-id="2af0a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2af0a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af0a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2af0a-121">-WhatIf</span></span>
<span data-ttu-id="2af0a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2af0a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2af0a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2af0a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2af0a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af0a-124">-DefaultProfile</span></span>
<span data-ttu-id="2af0a-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2af0a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2af0a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af0a-126">CommonParameters</span></span>
<span data-ttu-id="2af0a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2af0a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af0a-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2af0a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af0a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2af0a-129">INPUTS</span></span>

## <span data-ttu-id="2af0a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2af0a-130">OUTPUTS</span></span>

### <span data-ttu-id="2af0a-131">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="2af0a-131">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="2af0a-132">Note</span><span class="sxs-lookup"><span data-stu-id="2af0a-132">NOTES</span></span>

## <span data-ttu-id="2af0a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2af0a-133">RELATED LINKS</span></span>

[<span data-ttu-id="2af0a-134">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2af0a-134">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="2af0a-135">Registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2af0a-135">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="2af0a-136">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2af0a-136">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


