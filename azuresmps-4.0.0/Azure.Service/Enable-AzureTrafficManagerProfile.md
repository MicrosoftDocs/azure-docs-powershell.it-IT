---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029837"
---
# <span data-ttu-id="64ae2-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="64ae2-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="64ae2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="64ae2-103">Abilita un profilo di Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="64ae2-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="64ae2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64ae2-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64ae2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64ae2-105">DESCRIPTION</span></span>
<span data-ttu-id="64ae2-106">Il cmdlet **Enable-AzureTrafficManagerProfile** Abilita un profilo di Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="64ae2-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="64ae2-107">Specifica il parametro *PassThru* per visualizzare se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="64ae2-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="64ae2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64ae2-108">EXAMPLES</span></span>

### <span data-ttu-id="64ae2-109">Esempio 1: abilitare un profilo di Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="64ae2-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="64ae2-110">Questo comando consente al profilo di gestione traffico denominato profilo.</span><span class="sxs-lookup"><span data-stu-id="64ae2-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="64ae2-111">Esempio 2: abilitare un profilo di Traffic Manager e visualizzare i risultati</span><span class="sxs-lookup"><span data-stu-id="64ae2-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="64ae2-112">Questo comando consente al profilo di gestione traffico denominato profilo e indica se il comando è stato completato.</span><span class="sxs-lookup"><span data-stu-id="64ae2-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="64ae2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64ae2-113">PARAMETERS</span></span>

### <span data-ttu-id="64ae2-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="64ae2-114">-Name</span></span>
<span data-ttu-id="64ae2-115">Specifica il nome del profilo di Traffic Manager da abilitare.</span><span class="sxs-lookup"><span data-stu-id="64ae2-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="64ae2-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64ae2-116">-PassThru</span></span>
<span data-ttu-id="64ae2-117">Restituisce $True se l'operazione è riuscita; in caso contrario, $False.</span><span class="sxs-lookup"><span data-stu-id="64ae2-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="64ae2-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="64ae2-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="64ae2-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="64ae2-119">-Profile</span></span>
<span data-ttu-id="64ae2-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64ae2-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="64ae2-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="64ae2-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64ae2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ae2-122">CommonParameters</span></span>
<span data-ttu-id="64ae2-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ae2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ae2-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64ae2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ae2-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64ae2-125">INPUTS</span></span>

## <span data-ttu-id="64ae2-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64ae2-126">OUTPUTS</span></span>

### <span data-ttu-id="64ae2-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64ae2-127">System.Boolean</span></span>
<span data-ttu-id="64ae2-128">Questo cmdlet genera $True o $False.</span><span class="sxs-lookup"><span data-stu-id="64ae2-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="64ae2-129">Se l'operazione viene eseguita correttamente e se specifichi il parametro *PassThru* , questo cmdlet restituisce un valore di $true.</span><span class="sxs-lookup"><span data-stu-id="64ae2-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="64ae2-130">Note</span><span class="sxs-lookup"><span data-stu-id="64ae2-130">NOTES</span></span>

## <span data-ttu-id="64ae2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64ae2-131">RELATED LINKS</span></span>

[<span data-ttu-id="64ae2-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="64ae2-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="64ae2-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="64ae2-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="64ae2-134">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="64ae2-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="64ae2-135">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="64ae2-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="64ae2-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="64ae2-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


