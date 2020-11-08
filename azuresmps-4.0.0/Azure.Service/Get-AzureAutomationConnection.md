---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029832"
---
# <span data-ttu-id="0ce88-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0ce88-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="0ce88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ce88-102">SYNOPSIS</span></span>

<span data-ttu-id="0ce88-103">Ottiene una connessione di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="0ce88-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="0ce88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ce88-104">SYNTAX</span></span>

### <span data-ttu-id="0ce88-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0ce88-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0ce88-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="0ce88-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ce88-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="0ce88-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ce88-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ce88-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0ce88-109">Il cmdlet **Get-AzureAutomationConnection** ottiene una o più connessioni di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0ce88-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="0ce88-110">Per impostazione predefinita, vengono restituite tutte le connessioni.</span><span class="sxs-lookup"><span data-stu-id="0ce88-110">By default, all connections are returned.</span></span>
<span data-ttu-id="0ce88-111">Per ottenere una connessione specifica, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="0ce88-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="0ce88-112">Per ottenere tutte le connessioni di un determinato tipo, specificare il nome del tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="0ce88-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="0ce88-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ce88-113">EXAMPLES</span></span>

### <span data-ttu-id="0ce88-114">Esempio 1: ottenere tutte le connessioni</span><span class="sxs-lookup"><span data-stu-id="0ce88-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0ce88-115">Questo comando consente di ottenere tutte le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0ce88-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0ce88-116">Esempio 2: ottenere tutte le connessioni di un tipo</span><span class="sxs-lookup"><span data-stu-id="0ce88-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="0ce88-117">Questo comando consente di ottenere tutte le connessioni Azure nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0ce88-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0ce88-118">Esempio 3: ottenere una connessione</span><span class="sxs-lookup"><span data-stu-id="0ce88-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="0ce88-119">Questo comando ottiene la connessione denominata connessione.</span><span class="sxs-lookup"><span data-stu-id="0ce88-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="0ce88-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ce88-120">PARAMETERS</span></span>

### <span data-ttu-id="0ce88-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ce88-121">-AutomationAccountName</span></span>
<span data-ttu-id="0ce88-122">Specifica il nome dell'account di automazione con la connessione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0ce88-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

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

### <span data-ttu-id="0ce88-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="0ce88-123">-ConnectionTypeName</span></span>
<span data-ttu-id="0ce88-124">Specifica il nome di un tipo di connessione per le connessioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0ce88-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce88-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ce88-125">-Name</span></span>
<span data-ttu-id="0ce88-126">Specifica il nome di una connessione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0ce88-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce88-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="0ce88-127">-Profile</span></span>
<span data-ttu-id="0ce88-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ce88-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ce88-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0ce88-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ce88-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce88-130">CommonParameters</span></span>
<span data-ttu-id="0ce88-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce88-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce88-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce88-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce88-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ce88-133">INPUTS</span></span>

## <span data-ttu-id="0ce88-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ce88-134">OUTPUTS</span></span>

### <span data-ttu-id="0ce88-135">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="0ce88-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="0ce88-136">Note</span><span class="sxs-lookup"><span data-stu-id="0ce88-136">NOTES</span></span>

## <span data-ttu-id="0ce88-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ce88-137">RELATED LINKS</span></span>

[<span data-ttu-id="0ce88-138">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0ce88-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="0ce88-139">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0ce88-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="0ce88-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="0ce88-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


