---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 76c1f255b2d8dc3275ec3a691337019a7fd1e3e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687951"
---
# <span data-ttu-id="fd9fd-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd9fd-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="fd9fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd9fd-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9fd-103">Rimuove un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd9fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd9fd-104">SYNTAX</span></span>

### <span data-ttu-id="fd9fd-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9fd-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd9fd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd9fd-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd9fd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd9fd-107">DESCRIPTION</span></span>
<span data-ttu-id="fd9fd-108">Il cmdlet **Remove-AzureRmCdnProfile** consente di rimuovere un profilo CDN (Azure Content delivering Network).</span><span class="sxs-lookup"><span data-stu-id="fd9fd-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="fd9fd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd9fd-109">EXAMPLES</span></span>

## <span data-ttu-id="fd9fd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd9fd-110">PARAMETERS</span></span>

### <span data-ttu-id="fd9fd-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd9fd-111">-CdnProfile</span></span>
<span data-ttu-id="fd9fd-112">Specifica il profilo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd9fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9fd-113">-DefaultProfile</span></span>
<span data-ttu-id="fd9fd-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fd9fd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9fd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd9fd-115">-Force</span></span>
<span data-ttu-id="fd9fd-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd9fd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd9fd-117">-PassThru</span></span>
<span data-ttu-id="fd9fd-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd9fd-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd9fd-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fd9fd-120">-ProfileName</span></span>
<span data-ttu-id="fd9fd-121">Specifica il nome del profilo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd9fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd9fd-123">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9fd-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd9fd-124">-Confirm</span></span>
<span data-ttu-id="fd9fd-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd9fd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd9fd-126">-WhatIf</span></span>
<span data-ttu-id="fd9fd-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd9fd-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd9fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9fd-129">CommonParameters</span></span>
<span data-ttu-id="fd9fd-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9fd-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd9fd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9fd-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd9fd-132">INPUTS</span></span>

### <span data-ttu-id="fd9fd-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="fd9fd-133">PSProfile</span></span>
<span data-ttu-id="fd9fd-134">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fd9fd-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="fd9fd-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd9fd-135">OUTPUTS</span></span>

### <span data-ttu-id="fd9fd-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd9fd-136">System.Boolean</span></span>

## <span data-ttu-id="fd9fd-137">Note</span><span class="sxs-lookup"><span data-stu-id="fd9fd-137">NOTES</span></span>

## <span data-ttu-id="fd9fd-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd9fd-138">RELATED LINKS</span></span>

[<span data-ttu-id="fd9fd-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd9fd-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="fd9fd-140">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd9fd-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="fd9fd-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fd9fd-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


