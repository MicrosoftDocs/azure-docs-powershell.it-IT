---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 829dc03dad037b6b1576613ab18d9929a777241e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509795"
---
# <span data-ttu-id="2bd48-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2bd48-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="2bd48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bd48-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd48-103">Rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="2bd48-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bd48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bd48-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bd48-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd48-106">Il cmdlet **Remove-AzureRmNetworkInterface** rimuove un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd48-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="2bd48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bd48-107">EXAMPLES</span></span>

### <span data-ttu-id="2bd48-108">Esempio 1: rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="2bd48-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="2bd48-109">Questo comando rimuove l'interfaccia di rete NetworkInterface1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="2bd48-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="2bd48-110">Poiché il parametro *Force* non viene usato, all'utente verrà richiesto di confermare questa azione.</span><span class="sxs-lookup"><span data-stu-id="2bd48-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="2bd48-111">Esempio 2: rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="2bd48-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="2bd48-112">Questo comando rimuove tutte le interfacce di rete nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="2bd48-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="2bd48-113">Poiché viene usato il parametro *Force* , all'utente non viene richiesto di confermare.</span><span class="sxs-lookup"><span data-stu-id="2bd48-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="2bd48-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bd48-114">PARAMETERS</span></span>

### <span data-ttu-id="2bd48-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bd48-115">-AsJob</span></span>
<span data-ttu-id="2bd48-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2bd48-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bd48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd48-117">-DefaultProfile</span></span>
<span data-ttu-id="2bd48-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd48-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bd48-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2bd48-119">-Force</span></span>
<span data-ttu-id="2bd48-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2bd48-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2bd48-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bd48-121">-Name</span></span>
<span data-ttu-id="2bd48-122">Specifica il nome dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd48-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bd48-123">-PassThru</span></span>
<span data-ttu-id="2bd48-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2bd48-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2bd48-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2bd48-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2bd48-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd48-126">-ResourceGroupName</span></span>
<span data-ttu-id="2bd48-127">Specifica il nome di un gruppo di risorse che contiene l'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd48-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2bd48-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2bd48-128">-Confirm</span></span>
<span data-ttu-id="2bd48-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd48-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd48-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd48-130">-WhatIf</span></span>
<span data-ttu-id="2bd48-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bd48-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bd48-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bd48-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd48-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd48-133">CommonParameters</span></span>
<span data-ttu-id="2bd48-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd48-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd48-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd48-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd48-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bd48-136">INPUTS</span></span>

### <span data-ttu-id="2bd48-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2bd48-137">None</span></span>
<span data-ttu-id="2bd48-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2bd48-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2bd48-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bd48-139">OUTPUTS</span></span>

## <span data-ttu-id="2bd48-140">Note</span><span class="sxs-lookup"><span data-stu-id="2bd48-140">NOTES</span></span>

## <span data-ttu-id="2bd48-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bd48-141">RELATED LINKS</span></span>

[<span data-ttu-id="2bd48-142">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2bd48-142">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="2bd48-143">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2bd48-143">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="2bd48-144">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2bd48-144">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


