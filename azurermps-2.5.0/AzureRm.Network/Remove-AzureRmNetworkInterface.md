---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 955c5200b7c7b9716e096f1157f7179619ae4f5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865890"
---
# <span data-ttu-id="25390-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="25390-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="25390-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25390-102">SYNOPSIS</span></span>
<span data-ttu-id="25390-103">Rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="25390-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25390-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25390-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25390-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25390-105">DESCRIPTION</span></span>
<span data-ttu-id="25390-106">Il cmdlet **Remove-AzureRmNetworkInterface** rimuove un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="25390-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="25390-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25390-107">EXAMPLES</span></span>

### <span data-ttu-id="25390-108">Esempio 1: rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="25390-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="25390-109">Questo comando rimuove l'interfaccia di rete NetworkInterface1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="25390-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="25390-110">Poiché il parametro *Force* non viene usato, all'utente verrà richiesto di confermare questa azione.</span><span class="sxs-lookup"><span data-stu-id="25390-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="25390-111">Esempio 2: rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="25390-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="25390-112">Questo comando rimuove tutte le interfacce di rete nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="25390-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="25390-113">Poiché viene usato il parametro *Force* , all'utente non viene richiesto di confermare.</span><span class="sxs-lookup"><span data-stu-id="25390-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="25390-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25390-114">PARAMETERS</span></span>

### <span data-ttu-id="25390-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25390-115">-AsJob</span></span>
<span data-ttu-id="25390-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="25390-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25390-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25390-117">-DefaultProfile</span></span>
<span data-ttu-id="25390-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25390-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25390-119">-Force</span><span class="sxs-lookup"><span data-stu-id="25390-119">-Force</span></span>
<span data-ttu-id="25390-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="25390-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25390-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="25390-121">-Name</span></span>
<span data-ttu-id="25390-122">Specifica il nome dell'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25390-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="25390-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25390-123">-PassThru</span></span>
<span data-ttu-id="25390-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="25390-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25390-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="25390-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25390-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25390-126">-ResourceGroupName</span></span>
<span data-ttu-id="25390-127">Specifica il nome di un gruppo di risorse che contiene l'interfaccia di rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25390-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="25390-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="25390-128">-Confirm</span></span>
<span data-ttu-id="25390-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25390-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25390-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25390-130">-WhatIf</span></span>
<span data-ttu-id="25390-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25390-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25390-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25390-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25390-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25390-133">CommonParameters</span></span>
<span data-ttu-id="25390-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25390-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25390-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25390-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25390-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25390-136">INPUTS</span></span>

## <span data-ttu-id="25390-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25390-137">OUTPUTS</span></span>

## <span data-ttu-id="25390-138">Note</span><span class="sxs-lookup"><span data-stu-id="25390-138">NOTES</span></span>

## <span data-ttu-id="25390-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25390-139">RELATED LINKS</span></span>

[<span data-ttu-id="25390-140">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="25390-140">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="25390-141">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="25390-141">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="25390-142">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="25390-142">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


