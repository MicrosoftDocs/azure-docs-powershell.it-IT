---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205027"
---
# <span data-ttu-id="b13c3-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b13c3-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="b13c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b13c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b13c3-103">Elimina un account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="b13c3-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="b13c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b13c3-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b13c3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b13c3-105">DESCRIPTION</span></span>
<span data-ttu-id="b13c3-106">Il cmdlet **Remove-AzCognitiveServicesAccount** elimina l'account di Servizi cognitivi specificato.</span><span class="sxs-lookup"><span data-stu-id="b13c3-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="b13c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b13c3-107">EXAMPLES</span></span>

### <span data-ttu-id="b13c3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b13c3-108">Example 1</span></span>
<span data-ttu-id="b13c3-109">Questo comando non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b13c3-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="b13c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b13c3-110">PARAMETERS</span></span>

### <span data-ttu-id="b13c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13c3-111">-DefaultProfile</span></span>
<span data-ttu-id="b13c3-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b13c3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13c3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b13c3-113">-Force</span></span>
<span data-ttu-id="b13c3-114">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b13c3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b13c3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b13c3-115">-Name</span></span>
<span data-ttu-id="b13c3-116">Specifica il nome dell'account da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b13c3-116">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13c3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13c3-117">-ResourceGroupName</span></span>
<span data-ttu-id="b13c3-118">Specifica il nome del gruppo di risorse a cui è assegnato l'account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="b13c3-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13c3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b13c3-119">-Confirm</span></span>
<span data-ttu-id="b13c3-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b13c3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b13c3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13c3-121">-WhatIf</span></span>
<span data-ttu-id="b13c3-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b13c3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13c3-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b13c3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b13c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13c3-124">CommonParameters</span></span>
<span data-ttu-id="b13c3-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13c3-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b13c3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13c3-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="b13c3-127">INPUTS</span></span>

### <span data-ttu-id="b13c3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b13c3-128">System.String</span></span>

## <span data-ttu-id="b13c3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b13c3-129">OUTPUTS</span></span>

### <span data-ttu-id="b13c3-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="b13c3-130">System.Void</span></span>

## <span data-ttu-id="b13c3-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="b13c3-131">NOTES</span></span>

## <span data-ttu-id="b13c3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b13c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="b13c3-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b13c3-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="b13c3-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b13c3-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="b13c3-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b13c3-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


