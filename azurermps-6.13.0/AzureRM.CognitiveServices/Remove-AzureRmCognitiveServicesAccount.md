---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 2c8496af209cc72ebb6cb9a2ed40ae6033ce7268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520672"
---
# <span data-ttu-id="804a5-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="804a5-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="804a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="804a5-102">SYNOPSIS</span></span>
<span data-ttu-id="804a5-103">Elimina un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="804a5-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="804a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="804a5-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="804a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="804a5-105">DESCRIPTION</span></span>
<span data-ttu-id="804a5-106">Il cmdlet **Remove-AzureRmCognitiveServicesAccount** Elimina l'account di servizi cognitivi specificato.</span><span class="sxs-lookup"><span data-stu-id="804a5-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="804a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="804a5-107">EXAMPLES</span></span>

### <span data-ttu-id="804a5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="804a5-108">Example 1</span></span>
<span data-ttu-id="804a5-109">Questo comando non restituisce nulla.</span><span class="sxs-lookup"><span data-stu-id="804a5-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="804a5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="804a5-110">PARAMETERS</span></span>

### <span data-ttu-id="804a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804a5-111">-DefaultProfile</span></span>
<span data-ttu-id="804a5-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="804a5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="804a5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="804a5-113">-Force</span></span>
<span data-ttu-id="804a5-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="804a5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="804a5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="804a5-115">-Name</span></span>
<span data-ttu-id="804a5-116">Specifica il nome dell'account da eliminare.</span><span class="sxs-lookup"><span data-stu-id="804a5-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="804a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="804a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="804a5-118">Specifica il nome del gruppo di risorse a cui è assegnato l'account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="804a5-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="804a5-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="804a5-119">-Confirm</span></span>
<span data-ttu-id="804a5-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="804a5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="804a5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="804a5-121">-WhatIf</span></span>
<span data-ttu-id="804a5-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="804a5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="804a5-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="804a5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="804a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804a5-124">CommonParameters</span></span>
<span data-ttu-id="804a5-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="804a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804a5-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804a5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804a5-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="804a5-127">INPUTS</span></span>

### <span data-ttu-id="804a5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="804a5-128">System.String</span></span>

## <span data-ttu-id="804a5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="804a5-129">OUTPUTS</span></span>

### <span data-ttu-id="804a5-130">System. void</span><span class="sxs-lookup"><span data-stu-id="804a5-130">System.Void</span></span>

## <span data-ttu-id="804a5-131">Note</span><span class="sxs-lookup"><span data-stu-id="804a5-131">NOTES</span></span>

## <span data-ttu-id="804a5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="804a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="804a5-133">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="804a5-133">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="804a5-134">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="804a5-134">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="804a5-135">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="804a5-135">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


