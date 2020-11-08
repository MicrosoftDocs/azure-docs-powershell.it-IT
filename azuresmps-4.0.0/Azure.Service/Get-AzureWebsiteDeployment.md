---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029971"
---
# <span data-ttu-id="3d8ed-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="3d8ed-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="3d8ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8ed-103">Ottiene le distribuzioni per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="3d8ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d8ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="3d8ed-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3d8ed-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3d8ed-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3d8ed-108">Ottiene le distribuzioni per un sito Web in Azure.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="3d8ed-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-109">EXAMPLES</span></span>

## <span data-ttu-id="3d8ed-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-110">PARAMETERS</span></span>

### <span data-ttu-id="3d8ed-111">-Commitid</span><span class="sxs-lookup"><span data-stu-id="3d8ed-111">-CommitId</span></span>
<span data-ttu-id="3d8ed-112">Specifica l'ID univoco per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-112">Specifies the unique ID for the deployment.</span></span>

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

### <span data-ttu-id="3d8ed-113">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="3d8ed-113">-Details</span></span>
<span data-ttu-id="3d8ed-114">Mostra informazioni dettagliate sulle distribuzioni.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-114">Shows detailed information about the deployments.</span></span>

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

### <span data-ttu-id="3d8ed-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="3d8ed-115">-MaxResults</span></span>
<span data-ttu-id="3d8ed-116">Specifica il numero più grande di risultati che si desidera venga restituito dal comando.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8ed-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d8ed-117">-Name</span></span>
<span data-ttu-id="3d8ed-118">Specifica il nome del sito Web per cui si vogliono ottenere informazioni sulla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-118">Specifies the name of the website for which you want to get deployment information.</span></span>

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

### <span data-ttu-id="3d8ed-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d8ed-119">-Profile</span></span>
<span data-ttu-id="3d8ed-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d8ed-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d8ed-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="3d8ed-122">-Slot</span></span>
<span data-ttu-id="3d8ed-123">Specifica il nome dello slot.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-123">Specifies the slot name.</span></span>

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

### <span data-ttu-id="3d8ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8ed-124">CommonParameters</span></span>
<span data-ttu-id="3d8ed-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8ed-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d8ed-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8ed-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-127">INPUTS</span></span>

## <span data-ttu-id="3d8ed-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d8ed-128">OUTPUTS</span></span>

## <span data-ttu-id="3d8ed-129">Note</span><span class="sxs-lookup"><span data-stu-id="3d8ed-129">NOTES</span></span>

## <span data-ttu-id="3d8ed-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d8ed-130">RELATED LINKS</span></span>

[<span data-ttu-id="3d8ed-131">Ripristinare-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="3d8ed-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


