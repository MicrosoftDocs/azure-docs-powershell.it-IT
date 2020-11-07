---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 52788c012a7da6013e58df924d1eda0a3aa5afcb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835056"
---
# <span data-ttu-id="35653-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="35653-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="35653-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35653-102">SYNOPSIS</span></span>
<span data-ttu-id="35653-103">Crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="35653-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="35653-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35653-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35653-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35653-105">DESCRIPTION</span></span>
<span data-ttu-id="35653-106">Il cmdlet **New-AzActivityLogAlertCondition** crea un nuovo oggetto condizione di avviso del log delle attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="35653-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="35653-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35653-107">EXAMPLES</span></span>

### <span data-ttu-id="35653-108">Esempio 1: creare un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="35653-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="35653-109">Questo comando crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="35653-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="35653-110">**Nota** : quando questo cmdlet viene usato con Set-AzActivityLogAlert almeno uno di questi oggetti, passati come parametri, deve avere il relativo campo uguale a "Category".</span><span class="sxs-lookup"><span data-stu-id="35653-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="35653-111">In caso contrario, il backend risponde con una 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="35653-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="35653-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35653-112">PARAMETERS</span></span>

### <span data-ttu-id="35653-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35653-113">-DefaultProfile</span></span>
<span data-ttu-id="35653-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="35653-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35653-115">-Uguale</span><span class="sxs-lookup"><span data-stu-id="35653-115">-Equal</span></span>
<span data-ttu-id="35653-116">Specifica la proprietà Equals per la condizione foglia.</span><span class="sxs-lookup"><span data-stu-id="35653-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="35653-117">-Campo</span><span class="sxs-lookup"><span data-stu-id="35653-117">-Field</span></span>
<span data-ttu-id="35653-118">Specifica il campo per la condizione.</span><span class="sxs-lookup"><span data-stu-id="35653-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="35653-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35653-119">CommonParameters</span></span>
<span data-ttu-id="35653-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35653-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35653-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35653-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35653-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35653-122">INPUTS</span></span>

### <span data-ttu-id="35653-123">System. String</span><span class="sxs-lookup"><span data-stu-id="35653-123">System.String</span></span>

## <span data-ttu-id="35653-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35653-124">OUTPUTS</span></span>

### <span data-ttu-id="35653-125">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="35653-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="35653-126">Note</span><span class="sxs-lookup"><span data-stu-id="35653-126">NOTES</span></span>

## <span data-ttu-id="35653-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35653-127">RELATED LINKS</span></span>

[<span data-ttu-id="35653-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="35653-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="35653-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="35653-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="35653-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="35653-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="35653-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="35653-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="35653-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="35653-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="35653-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="35653-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
