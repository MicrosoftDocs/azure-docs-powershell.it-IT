---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029686"
---
# <span data-ttu-id="93214-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="93214-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="93214-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93214-102">SYNOPSIS</span></span>

<span data-ttu-id="93214-103">Crea un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="93214-103">Creates an Automation account.</span></span>

## <span data-ttu-id="93214-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93214-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93214-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93214-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="93214-106">Il cmdlet **New-AzureAutomationAccount** crea un nuovo account in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="93214-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="93214-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93214-107">EXAMPLES</span></span>

### <span data-ttu-id="93214-108">Esempio 1: creare un account di automazione</span><span class="sxs-lookup"><span data-stu-id="93214-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="93214-109">Questo comando crea un account di automazione denominato MyAutomationAccount nell'area est degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="93214-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="93214-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93214-110">PARAMETERS</span></span>

### <span data-ttu-id="93214-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="93214-111">-Location</span></span>
<span data-ttu-id="93214-112">Specifica la posizione dell'account.</span><span class="sxs-lookup"><span data-stu-id="93214-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="93214-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="93214-113">-Name</span></span>
<span data-ttu-id="93214-114">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="93214-114">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="93214-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="93214-115">-Profile</span></span>
<span data-ttu-id="93214-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93214-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93214-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="93214-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93214-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93214-118">CommonParameters</span></span>
<span data-ttu-id="93214-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93214-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93214-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93214-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93214-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93214-121">INPUTS</span></span>

## <span data-ttu-id="93214-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93214-122">OUTPUTS</span></span>

### <span data-ttu-id="93214-123">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="93214-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="93214-124">Note</span><span class="sxs-lookup"><span data-stu-id="93214-124">NOTES</span></span>

## <span data-ttu-id="93214-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93214-125">RELATED LINKS</span></span>

[<span data-ttu-id="93214-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="93214-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="93214-127">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="93214-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


