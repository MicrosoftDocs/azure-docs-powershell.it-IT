---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 85cf08b0ade67042c4aa4c4c5ff3253b6af9f2ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338167"
---
# <span data-ttu-id="e8d62-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e8d62-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="e8d62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8d62-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d62-103">Crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="e8d62-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="e8d62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8d62-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8d62-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8d62-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d62-106">Il cmdlet **New-AzActivityLogAlertCondition** crea un nuovo oggetto condizione di avviso del log delle attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="e8d62-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="e8d62-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8d62-107">EXAMPLES</span></span>

### <span data-ttu-id="e8d62-108">Esempio 1: creare un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="e8d62-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="e8d62-109">Questo comando crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="e8d62-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="e8d62-110">**Nota**: quando questo cmdlet viene usato con [set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) , almeno uno di questi oggetti, passati come parametri, deve avere il relativo campo uguale a "Category".</span><span class="sxs-lookup"><span data-stu-id="e8d62-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="e8d62-111">In caso contrario, il backend risponde con una 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="e8d62-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="e8d62-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8d62-112">PARAMETERS</span></span>

### <span data-ttu-id="e8d62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d62-113">-DefaultProfile</span></span>
<span data-ttu-id="e8d62-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8d62-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8d62-115">-Uguale</span><span class="sxs-lookup"><span data-stu-id="e8d62-115">-Equal</span></span>
<span data-ttu-id="e8d62-116">Specifica la proprietà Equals per la condizione foglia.</span><span class="sxs-lookup"><span data-stu-id="e8d62-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="e8d62-117">-Campo</span><span class="sxs-lookup"><span data-stu-id="e8d62-117">-Field</span></span>
<span data-ttu-id="e8d62-118">Specifica il campo per la condizione.</span><span class="sxs-lookup"><span data-stu-id="e8d62-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="e8d62-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d62-119">CommonParameters</span></span>
<span data-ttu-id="e8d62-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8d62-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d62-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8d62-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d62-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8d62-122">INPUTS</span></span>

### <span data-ttu-id="e8d62-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e8d62-123">System.String</span></span>

## <span data-ttu-id="e8d62-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8d62-124">OUTPUTS</span></span>

### <span data-ttu-id="e8d62-125">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="e8d62-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="e8d62-126">Note</span><span class="sxs-lookup"><span data-stu-id="e8d62-126">NOTES</span></span>

## <span data-ttu-id="e8d62-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8d62-127">RELATED LINKS</span></span>

[<span data-ttu-id="e8d62-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e8d62-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e8d62-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e8d62-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="e8d62-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e8d62-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="e8d62-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e8d62-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="e8d62-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e8d62-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="e8d62-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e8d62-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
