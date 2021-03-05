---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: f18479f8cf42c68a7c8a8a5d9f45a4542a758212
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979901"
---
# <span data-ttu-id="ae182-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="ae182-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="ae182-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae182-102">SYNOPSIS</span></span>
<span data-ttu-id="ae182-103">Crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="ae182-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="ae182-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae182-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae182-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ae182-105">DESCRIPTION</span></span>
<span data-ttu-id="ae182-106">Il cmdlet **New-AzActivityLogAlertCondition crea** un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="ae182-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="ae182-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae182-107">EXAMPLES</span></span>

### <span data-ttu-id="ae182-108">Esempio 1: Creare un nuovo oggetto condizione di avviso nel log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="ae182-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="ae182-109">Questo comando crea un nuovo oggetto condizione di avviso nel log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="ae182-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="ae182-110">**NOTA:** quando questo cmdlet viene usato con [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) almeno uno di questi oggetti, passato come parametri, deve avere il campo uguale a "Category".</span><span class="sxs-lookup"><span data-stu-id="ae182-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="ae182-111">In caso contrario, il back-end risponde con un valore 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="ae182-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="ae182-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae182-112">PARAMETERS</span></span>

### <span data-ttu-id="ae182-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae182-113">-DefaultProfile</span></span>
<span data-ttu-id="ae182-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ae182-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae182-115">-Uguale a</span><span class="sxs-lookup"><span data-stu-id="ae182-115">-Equal</span></span>
<span data-ttu-id="ae182-116">Specifica la proprietà uguale a per la condizione foglia.</span><span class="sxs-lookup"><span data-stu-id="ae182-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="ae182-117">-Field</span><span class="sxs-lookup"><span data-stu-id="ae182-117">-Field</span></span>
<span data-ttu-id="ae182-118">Specifica il campo per la condizione.</span><span class="sxs-lookup"><span data-stu-id="ae182-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="ae182-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae182-119">CommonParameters</span></span>
<span data-ttu-id="ae182-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae182-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae182-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae182-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae182-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="ae182-122">INPUTS</span></span>

### <span data-ttu-id="ae182-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ae182-123">System.String</span></span>

## <span data-ttu-id="ae182-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae182-124">OUTPUTS</span></span>

### <span data-ttu-id="ae182-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="ae182-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="ae182-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="ae182-126">NOTES</span></span>

## <span data-ttu-id="ae182-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae182-127">RELATED LINKS</span></span>

[<span data-ttu-id="ae182-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ae182-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="ae182-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ae182-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="ae182-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ae182-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="ae182-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ae182-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="ae182-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ae182-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="ae182-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="ae182-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
