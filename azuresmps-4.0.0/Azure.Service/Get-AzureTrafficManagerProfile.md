---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023494"
---
# <span data-ttu-id="97e86-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97e86-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="97e86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97e86-102">SYNOPSIS</span></span>
<span data-ttu-id="97e86-103">Ottiene i dettagli di un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="97e86-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="97e86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97e86-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="97e86-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97e86-105">DESCRIPTION</span></span>
<span data-ttu-id="97e86-106">Il cmdlet **Get-AzureTrafficManagerProfile** ottiene i dettagli di un profilo di gestione traffico di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97e86-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="97e86-107">Se non specifichi il parametro *Name* , il cmdlet elenca i profili di Traffic Manager nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="97e86-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="97e86-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97e86-108">EXAMPLES</span></span>

### <span data-ttu-id="97e86-109">Esempio 1: ottenere l'elenco dei profili di Traffic Manager in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="97e86-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="97e86-110">Questo comando consente di ottenere l'elenco dei profili di Traffic Manager nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97e86-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="97e86-111">Esempio 2: ottenere un profilo di Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="97e86-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="97e86-112">Questo comando consente di ottenere il profilo Traffic Manager denominato profilo.</span><span class="sxs-lookup"><span data-stu-id="97e86-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="97e86-113">Esempio 3: aggiungere un endpoint a un profilo di gestione traffico</span><span class="sxs-lookup"><span data-stu-id="97e86-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="97e86-114">Questo comando aggiunge un endpoint a un profilo di Traffic Manager e quindi Salva il profilo.</span><span class="sxs-lookup"><span data-stu-id="97e86-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="97e86-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97e86-115">PARAMETERS</span></span>

### <span data-ttu-id="97e86-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="97e86-116">-Name</span></span>
<span data-ttu-id="97e86-117">Specifica il nome del profilo di Traffic Manager da ottenere.</span><span class="sxs-lookup"><span data-stu-id="97e86-117">Specifies the name of the Traffic Manager profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e86-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="97e86-118">-Profile</span></span>
<span data-ttu-id="97e86-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97e86-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="97e86-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="97e86-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97e86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e86-121">CommonParameters</span></span>
<span data-ttu-id="97e86-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e86-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e86-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e86-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97e86-124">INPUTS</span></span>

## <span data-ttu-id="97e86-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97e86-125">OUTPUTS</span></span>

### <span data-ttu-id="97e86-126">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="97e86-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="97e86-127">Questo cmdlet genera un oggetto o oggetti del profilo di Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="97e86-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="97e86-128">Note</span><span class="sxs-lookup"><span data-stu-id="97e86-128">NOTES</span></span>

## <span data-ttu-id="97e86-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97e86-129">RELATED LINKS</span></span>

[<span data-ttu-id="97e86-130">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="97e86-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="97e86-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97e86-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="97e86-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97e86-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="97e86-133">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97e86-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="97e86-134">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97e86-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="97e86-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97e86-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


