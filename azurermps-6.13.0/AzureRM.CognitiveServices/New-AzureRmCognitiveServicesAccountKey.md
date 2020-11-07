---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 4701ae347f5a6ea8cd294a0ff75efa51f4d1370d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686632"
---
# <span data-ttu-id="be05b-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="be05b-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="be05b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be05b-102">SYNOPSIS</span></span>
<span data-ttu-id="be05b-103">Rigenera una chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="be05b-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be05b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be05b-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be05b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be05b-105">DESCRIPTION</span></span>
<span data-ttu-id="be05b-106">Il cmdlet **New-AzureRmCognitiveServicesAccountKey** rigenera una chiave API per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="be05b-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="be05b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be05b-107">EXAMPLES</span></span>

### <span data-ttu-id="be05b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be05b-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="be05b-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be05b-109">PARAMETERS</span></span>

### <span data-ttu-id="be05b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be05b-110">-DefaultProfile</span></span>
<span data-ttu-id="be05b-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="be05b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be05b-112">-Force</span><span class="sxs-lookup"><span data-stu-id="be05b-112">-Force</span></span>
<span data-ttu-id="be05b-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="be05b-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be05b-114">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="be05b-114">-KeyName</span></span>
<span data-ttu-id="be05b-115">Specifica il nome della chiave da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="be05b-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="be05b-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="be05b-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be05b-117">Key1</span><span class="sxs-lookup"><span data-stu-id="be05b-117">Key1</span></span>
- <span data-ttu-id="be05b-118">Key2</span><span class="sxs-lookup"><span data-stu-id="be05b-118">Key2</span></span>

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

### <span data-ttu-id="be05b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="be05b-119">-Name</span></span>
<span data-ttu-id="be05b-120">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="be05b-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="be05b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be05b-121">-ResourceGroupName</span></span>
<span data-ttu-id="be05b-122">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="be05b-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="be05b-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be05b-123">-Confirm</span></span>
<span data-ttu-id="be05b-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be05b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be05b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be05b-125">-WhatIf</span></span>
<span data-ttu-id="be05b-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be05b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be05b-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be05b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be05b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be05b-128">CommonParameters</span></span>
<span data-ttu-id="be05b-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be05b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be05b-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be05b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be05b-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be05b-131">INPUTS</span></span>

### <span data-ttu-id="be05b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="be05b-132">System.String</span></span>

### <span data-ttu-id="be05b-133">Microsoft. Azure. Management. CognitiveServices. Models. nome</span><span class="sxs-lookup"><span data-stu-id="be05b-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="be05b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be05b-134">OUTPUTS</span></span>

### <span data-ttu-id="be05b-135">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="be05b-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="be05b-136">Note</span><span class="sxs-lookup"><span data-stu-id="be05b-136">NOTES</span></span>

## <span data-ttu-id="be05b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be05b-137">RELATED LINKS</span></span>

[<span data-ttu-id="be05b-138">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="be05b-138">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


