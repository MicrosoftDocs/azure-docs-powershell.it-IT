---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CEFFEF9F-4500-447E-99F1-FE053AED880A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e5b65a88e41ce08ec1d60bc140828963950f447
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023556"
---
# <span data-ttu-id="99a70-101">Get-AzureServiceProjectRoleRuntime</span><span class="sxs-lookup"><span data-stu-id="99a70-101">Get-AzureServiceProjectRoleRuntime</span></span>

## <span data-ttu-id="99a70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99a70-102">SYNOPSIS</span></span>
<span data-ttu-id="99a70-103">Ottenere i runtime disponibili per l'installazione in un ruolo.</span><span class="sxs-lookup"><span data-stu-id="99a70-103">Get the runtimes available to install in a role.</span></span>

## <span data-ttu-id="99a70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99a70-104">SYNTAX</span></span>

```
Get-AzureServiceProjectRoleRuntime [-Runtime <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99a70-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99a70-105">DESCRIPTION</span></span>
<span data-ttu-id="99a70-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99a70-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="99a70-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="99a70-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="99a70-108">Ottiene i runtime disponibili per l'installazione in un ruolo.</span><span class="sxs-lookup"><span data-stu-id="99a70-108">Gets the runtimes available to install in a role.</span></span>

## <span data-ttu-id="99a70-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99a70-109">EXAMPLES</span></span>

## <span data-ttu-id="99a70-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99a70-110">PARAMETERS</span></span>

### <span data-ttu-id="99a70-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="99a70-111">-Profile</span></span>
<span data-ttu-id="99a70-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99a70-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99a70-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="99a70-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99a70-114">-Runtime</span><span class="sxs-lookup"><span data-stu-id="99a70-114">-Runtime</span></span>
<span data-ttu-id="99a70-115">Nome del runtime.</span><span class="sxs-lookup"><span data-stu-id="99a70-115">The name of the runtime.</span></span>
<span data-ttu-id="99a70-116">Se viene specificato un runtime, verranno restituite solo le versioni specifiche di tale runtime disponibili per l'installazione nel ruolo in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="99a70-116">If a runtime specified, only the specific versions of that runtime available to install in your role in Windows Azure will be returned.</span></span>

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

### <span data-ttu-id="99a70-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a70-117">CommonParameters</span></span>
<span data-ttu-id="99a70-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a70-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a70-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99a70-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a70-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99a70-120">INPUTS</span></span>

## <span data-ttu-id="99a70-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99a70-121">OUTPUTS</span></span>

## <span data-ttu-id="99a70-122">Note</span><span class="sxs-lookup"><span data-stu-id="99a70-122">NOTES</span></span>

## <span data-ttu-id="99a70-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99a70-123">RELATED LINKS</span></span>

[<span data-ttu-id="99a70-124">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="99a70-124">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="99a70-125">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="99a70-125">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="99a70-126">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="99a70-126">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)

[<span data-ttu-id="99a70-127">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="99a70-127">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


