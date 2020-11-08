---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029954"
---
# <span data-ttu-id="5a921-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5a921-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="5a921-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a921-102">SYNOPSIS</span></span>

<span data-ttu-id="5a921-103">Rimuove una connessione dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="5a921-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="5a921-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a921-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a921-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a921-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5a921-106">Il cmdlet **Remove-AzureAutomationConnection** rimuove una connessione da Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5a921-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="5a921-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a921-107">EXAMPLES</span></span>

### <span data-ttu-id="5a921-108">Esempio 1: rimuovere una connessione</span><span class="sxs-lookup"><span data-stu-id="5a921-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="5a921-109">Questo comando rimuove un certificato denominato connessione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5a921-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5a921-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a921-110">PARAMETERS</span></span>

### <span data-ttu-id="5a921-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5a921-111">-AutomationAccountName</span></span>
<span data-ttu-id="5a921-112">Specifica il nome dell'account di automazione con le credenziali.</span><span class="sxs-lookup"><span data-stu-id="5a921-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="5a921-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5a921-113">-Force</span></span>
<span data-ttu-id="5a921-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5a921-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a921-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a921-115">-Name</span></span>
<span data-ttu-id="5a921-116">Specifica il nome della connessione.</span><span class="sxs-lookup"><span data-stu-id="5a921-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="5a921-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="5a921-117">-Profile</span></span>
<span data-ttu-id="5a921-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a921-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a921-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5a921-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a921-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a921-120">CommonParameters</span></span>
<span data-ttu-id="5a921-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a921-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a921-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a921-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a921-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a921-123">INPUTS</span></span>

## <span data-ttu-id="5a921-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a921-124">OUTPUTS</span></span>

## <span data-ttu-id="5a921-125">Note</span><span class="sxs-lookup"><span data-stu-id="5a921-125">NOTES</span></span>

## <span data-ttu-id="5a921-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a921-126">RELATED LINKS</span></span>

[<span data-ttu-id="5a921-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5a921-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="5a921-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5a921-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="5a921-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="5a921-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


