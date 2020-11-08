---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029833"
---
# <span data-ttu-id="a4840-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a4840-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="a4840-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4840-102">SYNOPSIS</span></span>

<span data-ttu-id="a4840-103">Ottiene gli account di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="a4840-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="a4840-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4840-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4840-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4840-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a4840-106">Il cmdlet **Get-AzureAutomationAccount** ottiene gli account di automazione di Microsoft Azure per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a4840-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="a4840-107">Un account di automazione è un contenitore per le risorse di automazione che viene isolato dalle risorse di altri account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a4840-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="a4840-108">Le risorse di automazione includono manuali operativi, Jobs e asset.</span><span class="sxs-lookup"><span data-stu-id="a4840-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="a4840-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4840-109">EXAMPLES</span></span>

### <span data-ttu-id="a4840-110">Esempio 1: ottenere un account di automazione</span><span class="sxs-lookup"><span data-stu-id="a4840-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="a4840-111">Questo comando consente di ottenere l'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a4840-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a4840-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4840-112">PARAMETERS</span></span>

### <span data-ttu-id="a4840-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a4840-113">-Location</span></span>
<span data-ttu-id="a4840-114">Specifica una posizione di Azure associata agli account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a4840-114">Specifies an Azure location associated with Automation accounts.</span></span>

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

### <span data-ttu-id="a4840-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4840-115">-Name</span></span>
<span data-ttu-id="a4840-116">Specifica il nome di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4840-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4840-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="a4840-117">-Profile</span></span>
<span data-ttu-id="a4840-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4840-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a4840-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a4840-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a4840-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4840-120">CommonParameters</span></span>
<span data-ttu-id="a4840-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4840-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4840-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4840-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4840-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4840-123">INPUTS</span></span>

## <span data-ttu-id="a4840-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4840-124">OUTPUTS</span></span>

### <span data-ttu-id="a4840-125">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a4840-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="a4840-126">Note</span><span class="sxs-lookup"><span data-stu-id="a4840-126">NOTES</span></span>

## <span data-ttu-id="a4840-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4840-127">RELATED LINKS</span></span>

[<span data-ttu-id="a4840-128">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a4840-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="a4840-129">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a4840-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


