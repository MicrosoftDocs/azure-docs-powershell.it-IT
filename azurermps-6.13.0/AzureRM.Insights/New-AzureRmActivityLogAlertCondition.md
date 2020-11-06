---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 3904be513baf73c67c2dbd0018ae6b3e7e2226fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515252"
---
# <span data-ttu-id="27fe0-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="27fe0-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="27fe0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="27fe0-103">Crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="27fe0-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27fe0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27fe0-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27fe0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27fe0-105">DESCRIPTION</span></span>
<span data-ttu-id="27fe0-106">Il cmdlet **New-AzureRmActivityLogAlertCondition** crea un nuovo oggetto condizione di avviso del log delle attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="27fe0-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="27fe0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27fe0-107">EXAMPLES</span></span>

### <span data-ttu-id="27fe0-108">Esempio 1: creare un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="27fe0-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="27fe0-109">Questo comando crea un nuovo oggetto condizione di avviso del log attività in memoria.</span><span class="sxs-lookup"><span data-stu-id="27fe0-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="27fe0-110">**Nota** : quando questo cmdlet viene usato con Set-AzureRmActivityLogAlert almeno uno di questi oggetti, passati come parametri, deve avere il relativo campo uguale a "Category".</span><span class="sxs-lookup"><span data-stu-id="27fe0-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="27fe0-111">In caso contrario, il backend risponde con una 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="27fe0-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="27fe0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27fe0-112">PARAMETERS</span></span>

### <span data-ttu-id="27fe0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27fe0-113">-DefaultProfile</span></span>
<span data-ttu-id="27fe0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27fe0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27fe0-115">-Uguale</span><span class="sxs-lookup"><span data-stu-id="27fe0-115">-Equal</span></span>
<span data-ttu-id="27fe0-116">Specifica la proprietà Equals per la condizione foglia.</span><span class="sxs-lookup"><span data-stu-id="27fe0-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="27fe0-117">-Campo</span><span class="sxs-lookup"><span data-stu-id="27fe0-117">-Field</span></span>
<span data-ttu-id="27fe0-118">Specifica il campo per la condizione.</span><span class="sxs-lookup"><span data-stu-id="27fe0-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="27fe0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27fe0-119">CommonParameters</span></span>
<span data-ttu-id="27fe0-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27fe0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27fe0-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27fe0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27fe0-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27fe0-122">INPUTS</span></span>

### <span data-ttu-id="27fe0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="27fe0-123">System.String</span></span>

## <span data-ttu-id="27fe0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27fe0-124">OUTPUTS</span></span>

### <span data-ttu-id="27fe0-125">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="27fe0-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="27fe0-126">Note</span><span class="sxs-lookup"><span data-stu-id="27fe0-126">NOTES</span></span>

## <span data-ttu-id="27fe0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27fe0-127">RELATED LINKS</span></span>

[<span data-ttu-id="27fe0-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="27fe0-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="27fe0-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="27fe0-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="27fe0-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="27fe0-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="27fe0-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="27fe0-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="27fe0-132">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="27fe0-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="27fe0-133">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="27fe0-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
