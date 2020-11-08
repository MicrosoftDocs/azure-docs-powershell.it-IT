---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029889"
---
# <span data-ttu-id="ed25d-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="ed25d-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="ed25d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed25d-102">SYNOPSIS</span></span>

<span data-ttu-id="ed25d-103">Modifica il valore di un campo per una connessione.</span><span class="sxs-lookup"><span data-stu-id="ed25d-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="ed25d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed25d-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ed25d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed25d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ed25d-106">Il cmdlet **set-AzureAutomationConnectionFieldValue** modifica il valore di un campo per una connessione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ed25d-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="ed25d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed25d-107">EXAMPLES</span></span>

## <span data-ttu-id="ed25d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed25d-108">PARAMETERS</span></span>

### <span data-ttu-id="ed25d-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed25d-109">-AutomationAccountName</span></span>
<span data-ttu-id="ed25d-110">Specifica il nome dell'account di automazione con la connessione.</span><span class="sxs-lookup"><span data-stu-id="ed25d-110">Specifies the name of the Automation account with the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed25d-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="ed25d-111">-ConnectionFieldName</span></span>
<span data-ttu-id="ed25d-112">Specifica un nome per il campo.</span><span class="sxs-lookup"><span data-stu-id="ed25d-112">Specifies a name for the field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed25d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed25d-113">-Name</span></span>
<span data-ttu-id="ed25d-114">Specifica un nome per la connessione.</span><span class="sxs-lookup"><span data-stu-id="ed25d-114">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed25d-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="ed25d-115">-Profile</span></span>
<span data-ttu-id="ed25d-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed25d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed25d-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ed25d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed25d-118">-Valore</span><span class="sxs-lookup"><span data-stu-id="ed25d-118">-Value</span></span>
<span data-ttu-id="ed25d-119">Specifica un valore da archiviare nel campo Connection.</span><span class="sxs-lookup"><span data-stu-id="ed25d-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed25d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed25d-120">CommonParameters</span></span>
<span data-ttu-id="ed25d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed25d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed25d-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed25d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed25d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed25d-123">INPUTS</span></span>

## <span data-ttu-id="ed25d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed25d-124">OUTPUTS</span></span>

## <span data-ttu-id="ed25d-125">Note</span><span class="sxs-lookup"><span data-stu-id="ed25d-125">NOTES</span></span>

## <span data-ttu-id="ed25d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed25d-126">RELATED LINKS</span></span>

[<span data-ttu-id="ed25d-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="ed25d-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="ed25d-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="ed25d-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="ed25d-129">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="ed25d-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


