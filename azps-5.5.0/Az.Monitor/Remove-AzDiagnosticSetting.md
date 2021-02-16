---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180111"
---
# <span data-ttu-id="5255f-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5255f-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="5255f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5255f-102">SYNOPSIS</span></span>
<span data-ttu-id="5255f-103">Rimuovere un'impostazione diagnostica per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="5255f-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="5255f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5255f-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5255f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5255f-105">DESCRIPTION</span></span>
<span data-ttu-id="5255f-106">Il cmdlet **Remove-AzDiagnosticSetting** rimuove l'impostazione diagnostica per la risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="5255f-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="5255f-107">Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5255f-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5255f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5255f-108">EXAMPLES</span></span>

### <span data-ttu-id="5255f-109">Esempio 1: Rimuovere l'impostazione diagnostica predefinita (servizio) per una risorsa</span><span class="sxs-lookup"><span data-stu-id="5255f-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="5255f-110">Questo comando rimuove l'impostazione diagnostica predefinita (servizio) per la risorsa denominata Risorsa01.</span><span class="sxs-lookup"><span data-stu-id="5255f-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="5255f-111">Esempio 2: Rimuovere l'impostazione diagnostica predefinita identificata dal nome assegnato per una risorsa</span><span class="sxs-lookup"><span data-stu-id="5255f-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="5255f-112">Questo comando rimuove l'impostazione diagnostica denominata myDiagSetting per la risorsa Denominata Risorsa01.</span><span class="sxs-lookup"><span data-stu-id="5255f-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="5255f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5255f-113">PARAMETERS</span></span>

### <span data-ttu-id="5255f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5255f-114">-DefaultProfile</span></span>
<span data-ttu-id="5255f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5255f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5255f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5255f-116">-Name</span></span>
<span data-ttu-id="5255f-117">Nome dell'impostazione diagnostica.</span><span class="sxs-lookup"><span data-stu-id="5255f-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="5255f-118">Se la chiamata non viene specificata per impostazione predefinita su "servizio" come nell'API precedente e questo cmdlet disabilita solo tutte le categorie per metriche/log.</span><span class="sxs-lookup"><span data-stu-id="5255f-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="5255f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5255f-119">-ResourceId</span></span>
<span data-ttu-id="5255f-120">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5255f-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="5255f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5255f-121">-Confirm</span></span>
<span data-ttu-id="5255f-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5255f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5255f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5255f-123">-WhatIf</span></span>
<span data-ttu-id="5255f-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5255f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5255f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5255f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5255f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5255f-126">CommonParameters</span></span>
<span data-ttu-id="5255f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5255f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5255f-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5255f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5255f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="5255f-129">INPUTS</span></span>

### <span data-ttu-id="5255f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5255f-130">System.String</span></span>

## <span data-ttu-id="5255f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5255f-131">OUTPUTS</span></span>

### <span data-ttu-id="5255f-132">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5255f-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5255f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="5255f-133">NOTES</span></span>

## <span data-ttu-id="5255f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5255f-134">RELATED LINKS</span></span>

<span data-ttu-id="5255f-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="5255f-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
