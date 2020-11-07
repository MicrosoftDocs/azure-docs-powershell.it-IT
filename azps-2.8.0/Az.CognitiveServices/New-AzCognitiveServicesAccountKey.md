---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: ac8bc0e8fd65a82f05108351a5b3140da8c1fb3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675496"
---
# <span data-ttu-id="5c4f4-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="5c4f4-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="5c4f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4f4-103">Rigenera una chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-103">Regenerates an account key.</span></span>

## <span data-ttu-id="5c4f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c4f4-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c4f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="5c4f4-106">Il cmdlet **New-AzCognitiveServicesAccountKey** rigenera una chiave API per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="5c4f4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c4f4-107">EXAMPLES</span></span>

### <span data-ttu-id="5c4f4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c4f4-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="5c4f4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c4f4-109">PARAMETERS</span></span>

### <span data-ttu-id="5c4f4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c4f4-110">-DefaultProfile</span></span>
<span data-ttu-id="5c4f4-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5c4f4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c4f4-112">-Force</span><span class="sxs-lookup"><span data-stu-id="5c4f4-112">-Force</span></span>
<span data-ttu-id="5c4f4-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c4f4-114">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="5c4f4-114">-KeyName</span></span>
<span data-ttu-id="5c4f4-115">Specifica il nome della chiave da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="5c4f4-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c4f4-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c4f4-117">Key1</span><span class="sxs-lookup"><span data-stu-id="5c4f4-117">Key1</span></span>
- <span data-ttu-id="5c4f4-118">Key2</span><span class="sxs-lookup"><span data-stu-id="5c4f4-118">Key2</span></span>

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

### <span data-ttu-id="5c4f4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c4f4-119">-Name</span></span>
<span data-ttu-id="5c4f4-120">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="5c4f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c4f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="5c4f4-122">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="5c4f4-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c4f4-123">-Confirm</span></span>
<span data-ttu-id="5c4f4-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c4f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4f4-125">-WhatIf</span></span>
<span data-ttu-id="5c4f4-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4f4-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c4f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4f4-128">CommonParameters</span></span>
<span data-ttu-id="5c4f4-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c4f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4f4-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c4f4-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4f4-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c4f4-131">INPUTS</span></span>

### <span data-ttu-id="5c4f4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5c4f4-132">System.String</span></span>

### <span data-ttu-id="5c4f4-133">Microsoft. Azure. Management. CognitiveServices. Models. nome</span><span class="sxs-lookup"><span data-stu-id="5c4f4-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="5c4f4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c4f4-134">OUTPUTS</span></span>

### <span data-ttu-id="5c4f4-135">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5c4f4-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="5c4f4-136">Note</span><span class="sxs-lookup"><span data-stu-id="5c4f4-136">NOTES</span></span>

## <span data-ttu-id="5c4f4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c4f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="5c4f4-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="5c4f4-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


