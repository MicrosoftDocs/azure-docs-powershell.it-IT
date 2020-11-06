---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: f564a026359042a20e5d82e34425e98f1021422b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517020"
---
# <span data-ttu-id="345de-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="345de-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="345de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="345de-102">SYNOPSIS</span></span>
<span data-ttu-id="345de-103">Rimuove un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="345de-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="345de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="345de-104">SYNTAX</span></span>

### <span data-ttu-id="345de-105">Parametro set per i parametri dei campi</span><span class="sxs-lookup"><span data-stu-id="345de-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="345de-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="345de-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="345de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="345de-107">DESCRIPTION</span></span>
<span data-ttu-id="345de-108">Il cmdlet **Remove-AzureRmCdnProfile** consente di rimuovere un profilo CDN (Azure Content delivering Network).</span><span class="sxs-lookup"><span data-stu-id="345de-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="345de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="345de-109">EXAMPLES</span></span>

## <span data-ttu-id="345de-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="345de-110">PARAMETERS</span></span>

### <span data-ttu-id="345de-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="345de-111">-CdnProfile</span></span>
<span data-ttu-id="345de-112">Specifica il profilo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="345de-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="345de-113">-Force</span><span class="sxs-lookup"><span data-stu-id="345de-113">-Force</span></span>
<span data-ttu-id="345de-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="345de-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345de-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="345de-115">-PassThru</span></span>
<span data-ttu-id="345de-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="345de-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="345de-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="345de-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="345de-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="345de-118">-ProfileName</span></span>
<span data-ttu-id="345de-119">Specifica il nome del profilo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="345de-119">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="345de-120">-ResourceGroupName</span></span>
<span data-ttu-id="345de-121">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="345de-121">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345de-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="345de-122">-Confirm</span></span>
<span data-ttu-id="345de-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="345de-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="345de-124">-WhatIf</span></span>
<span data-ttu-id="345de-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="345de-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="345de-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="345de-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345de-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="345de-127">-DefaultProfile</span></span>
<span data-ttu-id="345de-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="345de-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="345de-129">CommonParameters</span></span>
<span data-ttu-id="345de-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="345de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="345de-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="345de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="345de-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="345de-132">INPUTS</span></span>

### <span data-ttu-id="345de-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="345de-133">PSProfile</span></span>
<span data-ttu-id="345de-134">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="345de-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="345de-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="345de-135">OUTPUTS</span></span>

### <span data-ttu-id="345de-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="345de-136">System.Boolean</span></span>

## <span data-ttu-id="345de-137">Note</span><span class="sxs-lookup"><span data-stu-id="345de-137">NOTES</span></span>

## <span data-ttu-id="345de-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="345de-138">RELATED LINKS</span></span>

[<span data-ttu-id="345de-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="345de-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="345de-140">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="345de-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="345de-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="345de-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


