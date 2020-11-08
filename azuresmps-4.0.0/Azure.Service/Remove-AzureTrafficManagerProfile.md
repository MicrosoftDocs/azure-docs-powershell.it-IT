---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029553"
---
# <span data-ttu-id="26f0c-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="26f0c-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="26f0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="26f0c-103">Rimuove un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="26f0c-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="26f0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26f0c-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="26f0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="26f0c-106">Il cmdlet **Remove-AzureTrafficManagerProfile** rimuove un profilo di Microsoft Azure Traffic Manager dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="26f0c-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="26f0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="26f0c-108">Esempio 1: rimuovere un profilo di Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="26f0c-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="26f0c-109">Questo comando rimuove il profilo di Traffic Manager denominato profilo.</span><span class="sxs-lookup"><span data-stu-id="26f0c-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="26f0c-110">Esempio 2: rimuovere un profilo di Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="26f0c-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="26f0c-111">Questo comando rimuove il profilo di Traffic Manager denominato profilo senza richiedere conferma e restituisce i risultati.</span><span class="sxs-lookup"><span data-stu-id="26f0c-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="26f0c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26f0c-112">PARAMETERS</span></span>

### <span data-ttu-id="26f0c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26f0c-113">-Force</span></span>
<span data-ttu-id="26f0c-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="26f0c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26f0c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="26f0c-115">-Name</span></span>
<span data-ttu-id="26f0c-116">Specifica il nome del profilo di Traffic Manager da eliminare.</span><span class="sxs-lookup"><span data-stu-id="26f0c-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="26f0c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26f0c-117">-PassThru</span></span>
<span data-ttu-id="26f0c-118">Restituisce $True se l'operazione è riuscita; in caso contrario, $False.</span><span class="sxs-lookup"><span data-stu-id="26f0c-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="26f0c-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="26f0c-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26f0c-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="26f0c-120">-Profile</span></span>
<span data-ttu-id="26f0c-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26f0c-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="26f0c-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="26f0c-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26f0c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f0c-123">CommonParameters</span></span>
<span data-ttu-id="26f0c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f0c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f0c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f0c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f0c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26f0c-126">INPUTS</span></span>

## <span data-ttu-id="26f0c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26f0c-127">OUTPUTS</span></span>

### <span data-ttu-id="26f0c-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26f0c-128">System.Boolean</span></span>
<span data-ttu-id="26f0c-129">Questo cmdlet genera $True o $False.</span><span class="sxs-lookup"><span data-stu-id="26f0c-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="26f0c-130">Se l'operazione riesce e se specifichi il parametro *PassThru* , questo cmdlet restituisce un valore di $true.</span><span class="sxs-lookup"><span data-stu-id="26f0c-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="26f0c-131">Note</span><span class="sxs-lookup"><span data-stu-id="26f0c-131">NOTES</span></span>

## <span data-ttu-id="26f0c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26f0c-132">RELATED LINKS</span></span>

[<span data-ttu-id="26f0c-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="26f0c-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="26f0c-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="26f0c-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="26f0c-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="26f0c-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="26f0c-136">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="26f0c-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="26f0c-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="26f0c-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


