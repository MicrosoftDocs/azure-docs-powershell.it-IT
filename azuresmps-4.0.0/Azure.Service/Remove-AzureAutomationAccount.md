---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029957"
---
# <span data-ttu-id="e47ad-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e47ad-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="e47ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e47ad-102">SYNOPSIS</span></span>

<span data-ttu-id="e47ad-103">Rimuove un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e47ad-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="e47ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e47ad-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e47ad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e47ad-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e47ad-106">Il cmdlet **Remove-AzureAutomationAccount** rimuove un account da Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e47ad-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e47ad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e47ad-107">EXAMPLES</span></span>

### <span data-ttu-id="e47ad-108">Esempio 1: rimuovere un account di automazione</span><span class="sxs-lookup"><span data-stu-id="e47ad-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="e47ad-109">Questo comando rimuove un account di automazione denominato MyAutomationAccount senza richiedere la convalida dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e47ad-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="e47ad-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e47ad-110">PARAMETERS</span></span>

### <span data-ttu-id="e47ad-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e47ad-111">-Force</span></span>
<span data-ttu-id="e47ad-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e47ad-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e47ad-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e47ad-113">-Name</span></span>
<span data-ttu-id="e47ad-114">Specifica il nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e47ad-114">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e47ad-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e47ad-115">-Profile</span></span>
<span data-ttu-id="e47ad-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e47ad-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e47ad-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e47ad-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e47ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47ad-118">CommonParameters</span></span>
<span data-ttu-id="e47ad-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e47ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47ad-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e47ad-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47ad-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e47ad-121">INPUTS</span></span>

## <span data-ttu-id="e47ad-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e47ad-122">OUTPUTS</span></span>

## <span data-ttu-id="e47ad-123">Note</span><span class="sxs-lookup"><span data-stu-id="e47ad-123">NOTES</span></span>

## <span data-ttu-id="e47ad-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e47ad-124">RELATED LINKS</span></span>

[<span data-ttu-id="e47ad-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e47ad-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="e47ad-126">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e47ad-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


