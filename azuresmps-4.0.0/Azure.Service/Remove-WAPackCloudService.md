---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030875"
---
# <span data-ttu-id="3b8c0-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3b8c0-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="3b8c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8c0-103">Rimuove gli oggetti del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="3b8c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b8c0-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b8c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b8c0-105">DESCRIPTION</span></span>
<span data-ttu-id="3b8c0-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="3b8c0-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3b8c0-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3b8c0-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3b8c0-109">Il cmdlet **Remove-WAPackCloudService** rimuove gli oggetti del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="3b8c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b8c0-110">EXAMPLES</span></span>

### <span data-ttu-id="3b8c0-111">Esempio 1: rimuovere un servizio cloud</span><span class="sxs-lookup"><span data-stu-id="3b8c0-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="3b8c0-112">Il primo comando ottiene il servizio cloud denominato ContosoCloudService01 usando il cmdlet **Get-WAPackCloudService** e quindi archivia tale oggetto nella variabile $CloudService.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="3b8c0-113">Il secondo comando rimuove la cloudservice archiviata in $CloudService.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="3b8c0-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="3b8c0-115">Esempio 2: rimuovere un servizio cloud senza conferma</span><span class="sxs-lookup"><span data-stu-id="3b8c0-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="3b8c0-116">Il primo comando ottiene il servizio cloud denominato ContosoCloudService02 usando il cmdlet **Get-WAPackCloudService** e quindi archivia tale oggetto nella variabile $CloudService.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="3b8c0-117">Il secondo comando rimuove il servizio cloud archiviato in $CloudService.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="3b8c0-118">Questo comando include il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="3b8c0-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="3b8c0-119">Il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3b8c0-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b8c0-120">PARAMETERS</span></span>

### <span data-ttu-id="3b8c0-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="3b8c0-121">-CloudService</span></span>
<span data-ttu-id="3b8c0-122">Specifica un oggetto servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="3b8c0-123">Per ottenere un servizio cloud, usare il cmdlet **Get-WAPackCloudService** .</span><span class="sxs-lookup"><span data-stu-id="3b8c0-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8c0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3b8c0-124">-Force</span></span>
<span data-ttu-id="3b8c0-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b8c0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b8c0-126">-PassThru</span></span>
<span data-ttu-id="3b8c0-127">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b8c0-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b8c0-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="3b8c0-129">-Profile</span></span>
<span data-ttu-id="3b8c0-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b8c0-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b8c0-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b8c0-132">-Confirm</span></span>
<span data-ttu-id="3b8c0-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b8c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b8c0-134">-WhatIf</span></span>
<span data-ttu-id="3b8c0-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b8c0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b8c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8c0-137">CommonParameters</span></span>
<span data-ttu-id="3b8c0-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8c0-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b8c0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8c0-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b8c0-140">INPUTS</span></span>

## <span data-ttu-id="3b8c0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b8c0-141">OUTPUTS</span></span>

## <span data-ttu-id="3b8c0-142">Note</span><span class="sxs-lookup"><span data-stu-id="3b8c0-142">NOTES</span></span>

## <span data-ttu-id="3b8c0-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b8c0-143">RELATED LINKS</span></span>

[<span data-ttu-id="3b8c0-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3b8c0-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="3b8c0-145">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3b8c0-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


