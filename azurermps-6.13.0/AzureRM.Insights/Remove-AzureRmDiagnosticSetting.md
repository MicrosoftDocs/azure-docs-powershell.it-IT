---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2f62b33b7a5a2224f54be765d03f72fc1667cec1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520999"
---
# <span data-ttu-id="c1ca1-101">Remove-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="c1ca1-101">Remove-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="c1ca1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ca1-103">Rimuovere un'impostazione di diagnostica per la risorsa a.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-103">Remove a diagnostic setting for the a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1ca1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1ca1-104">SYNTAX</span></span>

```
Remove-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1ca1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1ca1-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ca1-106">Il cmdlet **Remove-AzureRmDiagnosticSetting** rimuove l'impostazione di diagnostica per la risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-106">The **Remove-AzureRmDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="c1ca1-107">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c1ca1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1ca1-108">EXAMPLES</span></span>

### <span data-ttu-id="c1ca1-109">Esempio 1: rimuovere l'impostazione di diagnostica predefinita (servizio) per una risorsa</span><span class="sxs-lookup"><span data-stu-id="c1ca1-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="c1ca1-110">Questo comando rimuove l'impostazione di diagnostica predefinita (servizio) per la risorsa denominata Resource01.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="c1ca1-111">Esempio 2: rimuovere l'impostazione di diagnostica predefinita identificata dal nome specificato per una risorsa</span><span class="sxs-lookup"><span data-stu-id="c1ca1-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="c1ca1-112">Questo comando rimuove l'impostazione di diagnostica denominata myDiagSetting per la risorsa denominata Resource01.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="c1ca1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1ca1-113">PARAMETERS</span></span>

### <span data-ttu-id="c1ca1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ca1-114">-DefaultProfile</span></span>
<span data-ttu-id="c1ca1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1ca1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1ca1-116">-Name</span></span>
<span data-ttu-id="c1ca1-117">Nome dell'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="c1ca1-118">Se non viene specificata la chiamata "Service" per impostazione predefinita, come nell'API precedente, questo cmdlet disattiverà solo tutte le categorie per metriche/registri.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ca1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1ca1-119">-ResourceId</span></span>
<span data-ttu-id="c1ca1-120">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="c1ca1-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1ca1-121">-Confirm</span></span>
<span data-ttu-id="c1ca1-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1ca1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ca1-123">-WhatIf</span></span>
<span data-ttu-id="c1ca1-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1ca1-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1ca1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ca1-126">CommonParameters</span></span>
<span data-ttu-id="c1ca1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ca1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ca1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ca1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ca1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1ca1-129">INPUTS</span></span>

### <span data-ttu-id="c1ca1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c1ca1-130">System.String</span></span>

## <span data-ttu-id="c1ca1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1ca1-131">OUTPUTS</span></span>

### <span data-ttu-id="c1ca1-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c1ca1-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c1ca1-133">Note</span><span class="sxs-lookup"><span data-stu-id="c1ca1-133">NOTES</span></span>

## <span data-ttu-id="c1ca1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1ca1-134">RELATED LINKS</span></span>

<span data-ttu-id="c1ca1-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="c1ca1-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span></span>
