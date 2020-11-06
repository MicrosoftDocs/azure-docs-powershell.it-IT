---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: 43a405e3e3cc6bd617ba9f9dee66dd3e8902e8e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518080"
---
# <span data-ttu-id="61b83-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61b83-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="61b83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61b83-102">SYNOPSIS</span></span>
<span data-ttu-id="61b83-103">Rimuove un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="61b83-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61b83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61b83-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61b83-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61b83-105">DESCRIPTION</span></span>
<span data-ttu-id="61b83-106">Il cmdlet **Remove-AzureRmIntegrationAccount** rimuove un account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61b83-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="61b83-107">Specificare il nome dell'account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61b83-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="61b83-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="61b83-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="61b83-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="61b83-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="61b83-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="61b83-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="61b83-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="61b83-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="61b83-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61b83-112">EXAMPLES</span></span>

### <span data-ttu-id="61b83-113">Esempio 1: rimuovere un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="61b83-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="61b83-114">Questo comando rimuove un account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="61b83-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="61b83-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61b83-115">PARAMETERS</span></span>

### <span data-ttu-id="61b83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b83-116">-DefaultProfile</span></span>
<span data-ttu-id="61b83-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="61b83-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61b83-118">-Force</span><span class="sxs-lookup"><span data-stu-id="61b83-118">-Force</span></span>
<span data-ttu-id="61b83-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="61b83-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61b83-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="61b83-120">-Name</span></span>
<span data-ttu-id="61b83-121">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="61b83-121">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b83-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61b83-122">-ResourceGroupName</span></span>
<span data-ttu-id="61b83-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61b83-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61b83-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61b83-124">-Confirm</span></span>
<span data-ttu-id="61b83-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61b83-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61b83-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61b83-126">-WhatIf</span></span>
<span data-ttu-id="61b83-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61b83-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61b83-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61b83-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61b83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b83-129">CommonParameters</span></span>
<span data-ttu-id="61b83-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61b83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b83-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b83-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b83-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61b83-132">INPUTS</span></span>

### <span data-ttu-id="61b83-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61b83-133">None</span></span>
<span data-ttu-id="61b83-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="61b83-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61b83-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61b83-135">OUTPUTS</span></span>

## <span data-ttu-id="61b83-136">Note</span><span class="sxs-lookup"><span data-stu-id="61b83-136">NOTES</span></span>

## <span data-ttu-id="61b83-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61b83-137">RELATED LINKS</span></span>

[<span data-ttu-id="61b83-138">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61b83-138">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="61b83-139">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61b83-139">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="61b83-140">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="61b83-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


