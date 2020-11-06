---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: 409a1eca9083c51f501293e4ca37150ce0c328e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517095"
---
# <span data-ttu-id="5181f-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="5181f-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="5181f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5181f-102">SYNOPSIS</span></span>
<span data-ttu-id="5181f-103">Rimuove un tipo di connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="5181f-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5181f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5181f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5181f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5181f-105">DESCRIPTION</span></span>
<span data-ttu-id="5181f-106">Il cmdlet **Remove-AzureRmAutomationConnectionType** rimuove un tipo di connessione da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5181f-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>

<span data-ttu-id="5181f-107">Tutte le connessioni associate al tipo di connessione eliminate diventano inutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="5181f-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="5181f-108">Rimuoverli, a meno che non si crei un nuovo tipo di connessione che soddisfi i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="5181f-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 

- <span data-ttu-id="5181f-109">Il tipo ha lo stesso nome del tipo di connessione originale.</span><span class="sxs-lookup"><span data-stu-id="5181f-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="5181f-110">Il tipo ha le stesse definizioni di campo del tipo di connessione originale.</span><span class="sxs-lookup"><span data-stu-id="5181f-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="5181f-111">Può avere campi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5181f-111">It can have additional fields.</span></span>

## <span data-ttu-id="5181f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5181f-112">EXAMPLES</span></span>

### <span data-ttu-id="5181f-113">Esempio 1: rimuovere un tipo di connessione</span><span class="sxs-lookup"><span data-stu-id="5181f-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5181f-114">Questo comando rimuove un tipo di connessione denominato ContosoConnectionType nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5181f-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5181f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5181f-115">PARAMETERS</span></span>

### <span data-ttu-id="5181f-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5181f-116">-AutomationAccountName</span></span>
<span data-ttu-id="5181f-117">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove un tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="5181f-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5181f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5181f-118">-Force</span></span>
<span data-ttu-id="5181f-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="5181f-119">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5181f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5181f-120">-Name</span></span>
<span data-ttu-id="5181f-121">Specifica il nome del tipo di connessione di automazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5181f-121">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5181f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5181f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5181f-123">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un tipo di connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="5181f-123">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="5181f-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5181f-124">-Confirm</span></span>
<span data-ttu-id="5181f-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5181f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5181f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5181f-126">-WhatIf</span></span>
<span data-ttu-id="5181f-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5181f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5181f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5181f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5181f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5181f-129">-DefaultProfile</span></span>
<span data-ttu-id="5181f-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5181f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5181f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5181f-131">CommonParameters</span></span>
<span data-ttu-id="5181f-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5181f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5181f-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5181f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5181f-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5181f-134">INPUTS</span></span>

## <span data-ttu-id="5181f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5181f-135">OUTPUTS</span></span>

## <span data-ttu-id="5181f-136">Note</span><span class="sxs-lookup"><span data-stu-id="5181f-136">NOTES</span></span>

## <span data-ttu-id="5181f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5181f-137">RELATED LINKS</span></span>

[<span data-ttu-id="5181f-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5181f-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


