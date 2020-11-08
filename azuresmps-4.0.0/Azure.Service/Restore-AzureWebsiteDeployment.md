---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023421"
---
# <span data-ttu-id="44dd2-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="44dd2-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="44dd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="44dd2-103">Ridistribuisce una distribuzione precedente di un sito Web in Azure.</span><span class="sxs-lookup"><span data-stu-id="44dd2-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="44dd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44dd2-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44dd2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="44dd2-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44dd2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="44dd2-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="44dd2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="44dd2-108">Il cmdlet **Restore-AzureWebsiteDeployment** ridistribuisce una distribuzione precedente di un sito Web in Azure.</span><span class="sxs-lookup"><span data-stu-id="44dd2-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="44dd2-109">Questo processo sostituisce la distribuzione corrente con la distribuzione selezionata.</span><span class="sxs-lookup"><span data-stu-id="44dd2-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="44dd2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44dd2-110">EXAMPLES</span></span>

### <span data-ttu-id="44dd2-111">Esempio 1: ridistribuire un sito</span><span class="sxs-lookup"><span data-stu-id="44dd2-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="44dd2-112">Questo comando ridistribuisce la distribuzione con ID f876543210 per il sito Web denominato ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="44dd2-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="44dd2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44dd2-113">PARAMETERS</span></span>

### <span data-ttu-id="44dd2-114">-Commitid</span><span class="sxs-lookup"><span data-stu-id="44dd2-114">-CommitId</span></span>
<span data-ttu-id="44dd2-115">Specifica l'identificatore della distribuzione da ridistribuire.</span><span class="sxs-lookup"><span data-stu-id="44dd2-115">Specifies the identifier of the deployment to redeploy.</span></span>

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

### <span data-ttu-id="44dd2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="44dd2-116">-Force</span></span>
<span data-ttu-id="44dd2-117">Se abilitata, ridistribuisce la distribuzione precedente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="44dd2-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

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

### <span data-ttu-id="44dd2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="44dd2-118">-Name</span></span>
<span data-ttu-id="44dd2-119">Specifica il nome del sito Web da ridistribuire.</span><span class="sxs-lookup"><span data-stu-id="44dd2-119">Specifies the name of the website to redeploy.</span></span>

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

### <span data-ttu-id="44dd2-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="44dd2-120">-Profile</span></span>
<span data-ttu-id="44dd2-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44dd2-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44dd2-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="44dd2-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44dd2-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="44dd2-123">-Slot</span></span>
<span data-ttu-id="44dd2-124">Specifica il nome dello slot.</span><span class="sxs-lookup"><span data-stu-id="44dd2-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="44dd2-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44dd2-125">-Confirm</span></span>
<span data-ttu-id="44dd2-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44dd2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44dd2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44dd2-127">-WhatIf</span></span>
<span data-ttu-id="44dd2-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44dd2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44dd2-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44dd2-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44dd2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44dd2-130">CommonParameters</span></span>
<span data-ttu-id="44dd2-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44dd2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44dd2-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44dd2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44dd2-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44dd2-133">INPUTS</span></span>

## <span data-ttu-id="44dd2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44dd2-134">OUTPUTS</span></span>

## <span data-ttu-id="44dd2-135">Note</span><span class="sxs-lookup"><span data-stu-id="44dd2-135">NOTES</span></span>

## <span data-ttu-id="44dd2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44dd2-136">RELATED LINKS</span></span>

[<span data-ttu-id="44dd2-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="44dd2-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="44dd2-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="44dd2-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


