---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4370FF88-E34F-499D-AF57-53C15B4EB6E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: e55d9e54dcaa0f547d64ec58b2772a581a8ec30a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029946"
---
# <span data-ttu-id="2b3d1-101">Remove-AzureAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="2b3d1-101">Remove-AzureAutomationConnectionType</span></span>

## <span data-ttu-id="2b3d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b3d1-102">SYNOPSIS</span></span>

<span data-ttu-id="2b3d1-103">Rimuove un tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="2b3d1-103">Removes a connection type.</span></span>

## <span data-ttu-id="2b3d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b3d1-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnectionType -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2b3d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b3d1-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="2b3d1-106">Il cmdlet **Remove-AzureAutomationConnectionType** rimuove un tipo di connessione di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2b3d1-106">The **Remove-AzureAutomationConnectionType** cmdlet removes an Azure Automation connection type.</span></span>

## <span data-ttu-id="2b3d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b3d1-107">EXAMPLES</span></span>

## <span data-ttu-id="2b3d1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b3d1-108">PARAMETERS</span></span>

### <span data-ttu-id="2b3d1-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2b3d1-109">-AutomationAccountName</span></span>
<span data-ttu-id="2b3d1-110">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="2b3d1-110">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="2b3d1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2b3d1-111">-Force</span></span>
<span data-ttu-id="2b3d1-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2b3d1-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b3d1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b3d1-113">-Name</span></span>
<span data-ttu-id="2b3d1-114">Specifica il nome del tipo di connessione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2b3d1-114">Specifies the name of the connection type to remove.</span></span>

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

### <span data-ttu-id="2b3d1-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="2b3d1-115">-Profile</span></span>
<span data-ttu-id="2b3d1-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3d1-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b3d1-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2b3d1-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b3d1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3d1-118">CommonParameters</span></span>
<span data-ttu-id="2b3d1-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3d1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3d1-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3d1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3d1-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b3d1-121">INPUTS</span></span>

## <span data-ttu-id="2b3d1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b3d1-122">OUTPUTS</span></span>

## <span data-ttu-id="2b3d1-123">Note</span><span class="sxs-lookup"><span data-stu-id="2b3d1-123">NOTES</span></span>

## <span data-ttu-id="2b3d1-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b3d1-124">RELATED LINKS</span></span>

