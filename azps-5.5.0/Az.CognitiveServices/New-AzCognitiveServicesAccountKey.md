---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205034"
---
# <span data-ttu-id="568d2-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="568d2-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="568d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="568d2-102">SYNOPSIS</span></span>
<span data-ttu-id="568d2-103">Rigenera una chiave account.</span><span class="sxs-lookup"><span data-stu-id="568d2-103">Regenerates an account key.</span></span>

## <span data-ttu-id="568d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="568d2-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="568d2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="568d2-105">DESCRIPTION</span></span>
<span data-ttu-id="568d2-106">Il cmdlet **New-AzCognitiveServicesAccountKey** rigenera una chiave API per un account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="568d2-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="568d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="568d2-107">EXAMPLES</span></span>

### <span data-ttu-id="568d2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="568d2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="568d2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="568d2-109">PARAMETERS</span></span>

### <span data-ttu-id="568d2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568d2-110">-DefaultProfile</span></span>
<span data-ttu-id="568d2-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="568d2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="568d2-112">-Force</span><span class="sxs-lookup"><span data-stu-id="568d2-112">-Force</span></span>
<span data-ttu-id="568d2-113">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="568d2-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="568d2-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="568d2-114">-KeyName</span></span>
<span data-ttu-id="568d2-115">Specifica il nome della chiave da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="568d2-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="568d2-116">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="568d2-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="568d2-117">Tasto1</span><span class="sxs-lookup"><span data-stu-id="568d2-117">Key1</span></span>
- <span data-ttu-id="568d2-118">Tasto2</span><span class="sxs-lookup"><span data-stu-id="568d2-118">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases:
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="568d2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="568d2-119">-Name</span></span>
<span data-ttu-id="568d2-120">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="568d2-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="568d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="568d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="568d2-122">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="568d2-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="568d2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="568d2-123">-Confirm</span></span>
<span data-ttu-id="568d2-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="568d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="568d2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="568d2-125">-WhatIf</span></span>
<span data-ttu-id="568d2-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="568d2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="568d2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="568d2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="568d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568d2-128">CommonParameters</span></span>
<span data-ttu-id="568d2-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="568d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568d2-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="568d2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568d2-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="568d2-131">INPUTS</span></span>

### <span data-ttu-id="568d2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="568d2-132">System.String</span></span>

### <span data-ttu-id="568d2-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span><span class="sxs-lookup"><span data-stu-id="568d2-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="568d2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="568d2-134">OUTPUTS</span></span>

### <span data-ttu-id="568d2-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="568d2-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="568d2-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="568d2-136">NOTES</span></span>

## <span data-ttu-id="568d2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="568d2-137">RELATED LINKS</span></span>

[<span data-ttu-id="568d2-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="568d2-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


