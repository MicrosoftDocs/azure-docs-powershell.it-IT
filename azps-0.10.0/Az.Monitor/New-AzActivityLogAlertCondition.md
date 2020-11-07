---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 0797246cb3f1feb4354b7f4df6a457bd18682e42
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861161"
---
# <span data-ttu-id="d6bea-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="d6bea-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="d6bea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6bea-102">SYNOPSIS</span></span>
<span data-ttu-id="d6bea-103">Crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="d6bea-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="d6bea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6bea-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6bea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6bea-105">DESCRIPTION</span></span>
<span data-ttu-id="d6bea-106">Il cmdlet **New-AzActivityLogAlertCondition** crea un nuovo oggetto condizione di avviso del log delle attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="d6bea-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="d6bea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6bea-107">EXAMPLES</span></span>

### <span data-ttu-id="d6bea-108">Esempio 1: creare un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="d6bea-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="d6bea-109">Questo comando crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="d6bea-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="d6bea-110">**Nota** : quando questo cmdlet viene usato con Set-AzActivityLogAlert almeno uno di questi oggetti, passati come parametri, deve avere il relativo campo uguale a "Category".</span><span class="sxs-lookup"><span data-stu-id="d6bea-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="d6bea-111">In caso contrario, il backend risponde con una 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="d6bea-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="d6bea-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6bea-112">PARAMETERS</span></span>

### <span data-ttu-id="d6bea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6bea-113">-DefaultProfile</span></span>
<span data-ttu-id="d6bea-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d6bea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6bea-115">-Uguale</span><span class="sxs-lookup"><span data-stu-id="d6bea-115">-Equal</span></span>
<span data-ttu-id="d6bea-116">Specifica la proprietà Equals per la condizione foglia.</span><span class="sxs-lookup"><span data-stu-id="d6bea-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="d6bea-117">-Campo</span><span class="sxs-lookup"><span data-stu-id="d6bea-117">-Field</span></span>
<span data-ttu-id="d6bea-118">Specifica il campo per la condizione.</span><span class="sxs-lookup"><span data-stu-id="d6bea-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="d6bea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6bea-119">CommonParameters</span></span>
<span data-ttu-id="d6bea-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6bea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6bea-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6bea-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6bea-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6bea-122">INPUTS</span></span>

### <span data-ttu-id="d6bea-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d6bea-123">System.String</span></span>

## <span data-ttu-id="d6bea-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6bea-124">OUTPUTS</span></span>

### <span data-ttu-id="d6bea-125">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="d6bea-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="d6bea-126">Note</span><span class="sxs-lookup"><span data-stu-id="d6bea-126">NOTES</span></span>

## <span data-ttu-id="d6bea-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6bea-127">RELATED LINKS</span></span>

[<span data-ttu-id="d6bea-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d6bea-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="d6bea-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d6bea-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="d6bea-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d6bea-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="d6bea-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d6bea-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="d6bea-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d6bea-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="d6bea-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="d6bea-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
