---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023651"
---
# <span data-ttu-id="29e7e-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29e7e-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="29e7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="29e7e-103">Disabilita un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="29e7e-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="29e7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29e7e-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="29e7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="29e7e-106">Il cmdlet **Disable-AzureTrafficManagerProfile Disabilita** un profilo di Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="29e7e-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="29e7e-107">Puoi usare il parametro *PassThru* per visualizzare se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="29e7e-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="29e7e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29e7e-108">EXAMPLES</span></span>

### <span data-ttu-id="29e7e-109">Esempio 1: disabilitare un profilo di Traffic Manager e visualizzare i risultati</span><span class="sxs-lookup"><span data-stu-id="29e7e-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="29e7e-110">Questo comando Disabilita il profilo di Traffic Manager denominato profilo.</span><span class="sxs-lookup"><span data-stu-id="29e7e-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="29e7e-111">Il comando specifica il parametro *PassThru* per visualizzare se il comando è stato completato.</span><span class="sxs-lookup"><span data-stu-id="29e7e-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="29e7e-112">Esempio 2: disabilitare un profilo di Traffic Manager e visualizzare nessun risultato</span><span class="sxs-lookup"><span data-stu-id="29e7e-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="29e7e-113">Questo comando Disabilita il profilo di gestione traffico denominato profilo, ma non Visualizza se il comando è riuscito.</span><span class="sxs-lookup"><span data-stu-id="29e7e-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="29e7e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29e7e-114">PARAMETERS</span></span>

### <span data-ttu-id="29e7e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="29e7e-115">-Name</span></span>
<span data-ttu-id="29e7e-116">Specifica il nome del profilo di Traffic Manager da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="29e7e-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="29e7e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29e7e-117">-PassThru</span></span>
<span data-ttu-id="29e7e-118">Restituisce $True se l'operazione è riuscita; in caso contrario, $False.</span><span class="sxs-lookup"><span data-stu-id="29e7e-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="29e7e-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="29e7e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29e7e-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="29e7e-120">-Profile</span></span>
<span data-ttu-id="29e7e-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29e7e-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="29e7e-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="29e7e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29e7e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e7e-123">CommonParameters</span></span>
<span data-ttu-id="29e7e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e7e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e7e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e7e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e7e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29e7e-126">INPUTS</span></span>

## <span data-ttu-id="29e7e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29e7e-127">OUTPUTS</span></span>

### <span data-ttu-id="29e7e-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29e7e-128">System.Boolean</span></span>
<span data-ttu-id="29e7e-129">Questo cmdlet genera $True o $False.</span><span class="sxs-lookup"><span data-stu-id="29e7e-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="29e7e-130">Se l'operazione riesce e se specifichi il parametro *PassThru* , questo cmdlet restituisce un valore di $true.</span><span class="sxs-lookup"><span data-stu-id="29e7e-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="29e7e-131">Note</span><span class="sxs-lookup"><span data-stu-id="29e7e-131">NOTES</span></span>

## <span data-ttu-id="29e7e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29e7e-132">RELATED LINKS</span></span>

[<span data-ttu-id="29e7e-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29e7e-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="29e7e-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29e7e-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="29e7e-135">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29e7e-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="29e7e-136">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29e7e-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="29e7e-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="29e7e-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


