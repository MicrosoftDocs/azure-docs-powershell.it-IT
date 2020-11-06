---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 7c77f11842c224a0a023215175f52bf451867296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521095"
---
# <span data-ttu-id="a7826-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a7826-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="a7826-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7826-102">SYNOPSIS</span></span>
<span data-ttu-id="a7826-103">Elimina un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="a7826-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7826-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7826-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7826-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7826-105">DESCRIPTION</span></span>
<span data-ttu-id="a7826-106">Il cmdlet **Remove-AzureRmCognitiveServicesAccount** Elimina l'account di servizi cognitivi specificato.</span><span class="sxs-lookup"><span data-stu-id="a7826-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="a7826-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7826-107">EXAMPLES</span></span>

## <span data-ttu-id="a7826-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7826-108">PARAMETERS</span></span>

### <span data-ttu-id="a7826-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7826-109">-DefaultProfile</span></span>
<span data-ttu-id="a7826-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a7826-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7826-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a7826-111">-Force</span></span>
<span data-ttu-id="a7826-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a7826-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7826-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7826-113">-Name</span></span>
<span data-ttu-id="a7826-114">Specifica il nome dell'account da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a7826-114">Specifies the name of the account to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7826-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7826-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7826-116">Specifica il nome del gruppo di risorse a cui è assegnato l'account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="a7826-116">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7826-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7826-117">-Confirm</span></span>
<span data-ttu-id="a7826-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7826-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7826-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7826-119">-WhatIf</span></span>
<span data-ttu-id="a7826-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7826-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7826-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7826-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7826-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7826-122">CommonParameters</span></span>
<span data-ttu-id="a7826-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7826-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7826-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7826-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7826-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7826-125">INPUTS</span></span>

### <span data-ttu-id="a7826-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7826-126">None</span></span>
<span data-ttu-id="a7826-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a7826-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7826-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7826-128">OUTPUTS</span></span>

## <span data-ttu-id="a7826-129">Note</span><span class="sxs-lookup"><span data-stu-id="a7826-129">NOTES</span></span>

## <span data-ttu-id="a7826-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7826-130">RELATED LINKS</span></span>

[<span data-ttu-id="a7826-131">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a7826-131">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a7826-132">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a7826-132">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a7826-133">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a7826-133">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


