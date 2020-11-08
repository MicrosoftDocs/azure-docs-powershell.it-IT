---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029682"
---
# <span data-ttu-id="0fecb-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0fecb-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="0fecb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fecb-102">SYNOPSIS</span></span>

<span data-ttu-id="0fecb-103">Crea una connessione in automazione.</span><span class="sxs-lookup"><span data-stu-id="0fecb-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="0fecb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fecb-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0fecb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fecb-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0fecb-106">Il cmdlet **New-AzureAutomationConnection** crea una connessione in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0fecb-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="0fecb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fecb-107">EXAMPLES</span></span>

## <span data-ttu-id="0fecb-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fecb-108">PARAMETERS</span></span>

### <span data-ttu-id="0fecb-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0fecb-109">-AutomationAccountName</span></span>
<span data-ttu-id="0fecb-110">Specifica il nome dell'account di automazione in cui verrà archiviata la connessione.</span><span class="sxs-lookup"><span data-stu-id="0fecb-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

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

### <span data-ttu-id="0fecb-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="0fecb-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="0fecb-112">Specifica una tabella hash che contiene coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="0fecb-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="0fecb-113">Le chiavi rappresentano i campi di connessione nel tipo di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="0fecb-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="0fecb-114">I valori rappresentano i valori specifici da archiviare per ogni campo di connessione per l'istanza di connessione.</span><span class="sxs-lookup"><span data-stu-id="0fecb-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fecb-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="0fecb-115">-ConnectionTypeName</span></span>
<span data-ttu-id="0fecb-116">Specifica il nome del tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="0fecb-116">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="0fecb-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fecb-117">-Description</span></span>
<span data-ttu-id="0fecb-118">Specifica una descrizione per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="0fecb-118">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fecb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fecb-119">-Name</span></span>
<span data-ttu-id="0fecb-120">Specifica un nome per la connessione.</span><span class="sxs-lookup"><span data-stu-id="0fecb-120">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="0fecb-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="0fecb-121">-Profile</span></span>
<span data-ttu-id="0fecb-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fecb-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0fecb-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0fecb-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0fecb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fecb-124">CommonParameters</span></span>
<span data-ttu-id="0fecb-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fecb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fecb-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fecb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fecb-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fecb-127">INPUTS</span></span>

## <span data-ttu-id="0fecb-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fecb-128">OUTPUTS</span></span>

### <span data-ttu-id="0fecb-129">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="0fecb-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="0fecb-130">Note</span><span class="sxs-lookup"><span data-stu-id="0fecb-130">NOTES</span></span>

## <span data-ttu-id="0fecb-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fecb-131">RELATED LINKS</span></span>

[<span data-ttu-id="0fecb-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0fecb-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="0fecb-133">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0fecb-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="0fecb-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="0fecb-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


