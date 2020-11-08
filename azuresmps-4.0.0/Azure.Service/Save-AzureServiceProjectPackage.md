---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023418"
---
# <span data-ttu-id="b28b3-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="b28b3-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="b28b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b28b3-102">SYNOPSIS</span></span>
<span data-ttu-id="b28b3-103">Pacchetti del progetto di servizio nel pacchetto cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="b28b3-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="b28b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b28b3-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b28b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b28b3-105">DESCRIPTION</span></span>
<span data-ttu-id="b28b3-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b28b3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b28b3-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b28b3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b28b3-108">Il cmdlet **Save-AzureServiceProjectPackage** consente di creare pacchetti del progetto di servizio in un pacchetto cloud di Azure (\*. cspkg).</span><span class="sxs-lookup"><span data-stu-id="b28b3-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="b28b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b28b3-109">EXAMPLES</span></span>

### <span data-ttu-id="b28b3-110">Esempio 1: creare un pacchetto di progetto di servizio</span><span class="sxs-lookup"><span data-stu-id="b28b3-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="b28b3-111">Questo esempio crea un \*. cspgk per un progetto di servizio denominato MyAzureServiceProject.</span><span class="sxs-lookup"><span data-stu-id="b28b3-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="b28b3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b28b3-112">PARAMETERS</span></span>

### <span data-ttu-id="b28b3-113">-Local</span><span class="sxs-lookup"><span data-stu-id="b28b3-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28b3-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="b28b3-114">-Profile</span></span>
<span data-ttu-id="b28b3-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b28b3-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b28b3-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b28b3-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b28b3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28b3-117">CommonParameters</span></span>
<span data-ttu-id="b28b3-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b28b3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28b3-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b28b3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28b3-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b28b3-120">INPUTS</span></span>

## <span data-ttu-id="b28b3-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b28b3-121">OUTPUTS</span></span>

## <span data-ttu-id="b28b3-122">Note</span><span class="sxs-lookup"><span data-stu-id="b28b3-122">NOTES</span></span>

## <span data-ttu-id="b28b3-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b28b3-123">RELATED LINKS</span></span>

[<span data-ttu-id="b28b3-124">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b28b3-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


