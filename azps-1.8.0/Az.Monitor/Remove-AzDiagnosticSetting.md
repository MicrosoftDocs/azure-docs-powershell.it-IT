---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f99a7cfb18b585e1187cac62eb586bac37dad55d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678753"
---
# <span data-ttu-id="5264a-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5264a-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="5264a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5264a-102">SYNOPSIS</span></span>
<span data-ttu-id="5264a-103">Rimuovere un'impostazione di diagnostica per la risorsa a.</span><span class="sxs-lookup"><span data-stu-id="5264a-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="5264a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5264a-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5264a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5264a-105">DESCRIPTION</span></span>
<span data-ttu-id="5264a-106">Il cmdlet **Remove-AzDiagnosticSetting** rimuove l'impostazione di diagnostica per la risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="5264a-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="5264a-107">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5264a-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5264a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5264a-108">EXAMPLES</span></span>

### <span data-ttu-id="5264a-109">Esempio 1: rimuovere l'impostazione di diagnostica predefinita (servizio) per una risorsa</span><span class="sxs-lookup"><span data-stu-id="5264a-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="5264a-110">Questo comando rimuove l'impostazione di diagnostica predefinita (servizio) per la risorsa denominata Resource01.</span><span class="sxs-lookup"><span data-stu-id="5264a-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="5264a-111">Esempio 2: rimuovere l'impostazione di diagnostica predefinita identificata dal nome specificato per una risorsa</span><span class="sxs-lookup"><span data-stu-id="5264a-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="5264a-112">Questo comando rimuove l'impostazione di diagnostica denominata myDiagSetting per la risorsa denominata Resource01.</span><span class="sxs-lookup"><span data-stu-id="5264a-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="5264a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5264a-113">PARAMETERS</span></span>

### <span data-ttu-id="5264a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5264a-114">-DefaultProfile</span></span>
<span data-ttu-id="5264a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5264a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5264a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5264a-116">-Name</span></span>
<span data-ttu-id="5264a-117">Nome dell'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="5264a-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="5264a-118">Se non viene specificata la chiamata "Service" per impostazione predefinita, come nell'API precedente, questo cmdlet disattiverà solo tutte le categorie per metriche/registri.</span><span class="sxs-lookup"><span data-stu-id="5264a-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="5264a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5264a-119">-ResourceId</span></span>
<span data-ttu-id="5264a-120">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5264a-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="5264a-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5264a-121">-Confirm</span></span>
<span data-ttu-id="5264a-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5264a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5264a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5264a-123">-WhatIf</span></span>
<span data-ttu-id="5264a-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5264a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5264a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5264a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5264a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5264a-126">CommonParameters</span></span>
<span data-ttu-id="5264a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5264a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5264a-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5264a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5264a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5264a-129">INPUTS</span></span>

### <span data-ttu-id="5264a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5264a-130">System.String</span></span>

## <span data-ttu-id="5264a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5264a-131">OUTPUTS</span></span>

### <span data-ttu-id="5264a-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5264a-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5264a-133">Note</span><span class="sxs-lookup"><span data-stu-id="5264a-133">NOTES</span></span>

## <span data-ttu-id="5264a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5264a-134">RELATED LINKS</span></span>

<span data-ttu-id="5264a-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="5264a-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
