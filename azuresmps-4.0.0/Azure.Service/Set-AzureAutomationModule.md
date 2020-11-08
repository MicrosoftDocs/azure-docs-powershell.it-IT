---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023788"
---
# <span data-ttu-id="0b7f6-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0b7f6-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="0b7f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b7f6-102">SYNOPSIS</span></span>

<span data-ttu-id="0b7f6-103">Aggiorna un modulo in automazione.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="0b7f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b7f6-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b7f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b7f6-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0b7f6-106">Il cmdlet **set-AzureAutomationModule** importa una nuova versione di un modulo o modifica la configurazione del modulo in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="0b7f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b7f6-107">EXAMPLES</span></span>

### <span data-ttu-id="0b7f6-108">Esempio 1: aggiornare un modulo</span><span class="sxs-lookup"><span data-stu-id="0b7f6-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="0b7f6-109">Questo comando importa una versione aggiornata di un modulo esistente denominato ContosoModule nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="0b7f6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b7f6-110">PARAMETERS</span></span>

### <span data-ttu-id="0b7f6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0b7f6-111">-AutomationAccountName</span></span>
<span data-ttu-id="0b7f6-112">Specifica il nome dell'account di automazione con il modulo.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="0b7f6-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="0b7f6-113">-ContentLinkUri</span></span>
<span data-ttu-id="0b7f6-114">Specifica il percorso del file del modulo.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7f6-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="0b7f6-115">-ContentLinkVersion</span></span>
<span data-ttu-id="0b7f6-116">Specifica la versione del modulo.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-116">Specifies the version of the module.</span></span>

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

### <span data-ttu-id="0b7f6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b7f6-117">-Name</span></span>
<span data-ttu-id="0b7f6-118">Specifica il nome del modulo.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="0b7f6-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="0b7f6-119">-Profile</span></span>
<span data-ttu-id="0b7f6-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b7f6-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b7f6-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b7f6-122">-Tags</span></span>
<span data-ttu-id="0b7f6-123">Specifica i contrassegni per il modulo.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-123">Specifies tags for the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7f6-124">CommonParameters</span></span>
<span data-ttu-id="0b7f6-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7f6-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b7f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7f6-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b7f6-127">INPUTS</span></span>

### <span data-ttu-id="0b7f6-128">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="0b7f6-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="0b7f6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b7f6-129">OUTPUTS</span></span>

## <span data-ttu-id="0b7f6-130">Note</span><span class="sxs-lookup"><span data-stu-id="0b7f6-130">NOTES</span></span>

## <span data-ttu-id="0b7f6-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b7f6-131">RELATED LINKS</span></span>

[<span data-ttu-id="0b7f6-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0b7f6-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="0b7f6-133">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0b7f6-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="0b7f6-134">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0b7f6-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


