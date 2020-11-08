---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029942"
---
# <span data-ttu-id="db262-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="db262-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="db262-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db262-102">SYNOPSIS</span></span>

<span data-ttu-id="db262-103">Rimuove una credenziale dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="db262-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="db262-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db262-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db262-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db262-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="db262-106">Il cmdlet **Remove-AzureAutomationCredential** consente di rimuovere una credenziale da Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="db262-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="db262-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db262-107">EXAMPLES</span></span>

### <span data-ttu-id="db262-108">Esempio 1: rimuovere una credenziale</span><span class="sxs-lookup"><span data-stu-id="db262-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="db262-109">Questo comando consente di rimuovere una credenziale denominata credenziali nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="db262-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="db262-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db262-110">PARAMETERS</span></span>

### <span data-ttu-id="db262-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="db262-111">-AutomationAccountName</span></span>
<span data-ttu-id="db262-112">Specifica il nome dell'account di automazione con le credenziali.</span><span class="sxs-lookup"><span data-stu-id="db262-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="db262-113">-Force</span><span class="sxs-lookup"><span data-stu-id="db262-113">-Force</span></span>
<span data-ttu-id="db262-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="db262-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db262-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="db262-115">-Name</span></span>
<span data-ttu-id="db262-116">Specifica il nome della credenziale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="db262-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="db262-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="db262-117">-Profile</span></span>
<span data-ttu-id="db262-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db262-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db262-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="db262-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db262-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db262-120">CommonParameters</span></span>
<span data-ttu-id="db262-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db262-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db262-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db262-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db262-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db262-123">INPUTS</span></span>

## <span data-ttu-id="db262-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db262-124">OUTPUTS</span></span>

## <span data-ttu-id="db262-125">Note</span><span class="sxs-lookup"><span data-stu-id="db262-125">NOTES</span></span>

## <span data-ttu-id="db262-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db262-126">RELATED LINKS</span></span>

[<span data-ttu-id="db262-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="db262-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="db262-128">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="db262-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="db262-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="db262-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


