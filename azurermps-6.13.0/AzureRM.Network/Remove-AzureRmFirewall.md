---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
ms.openlocfilehash: 1a6c5ae69ef6aa6dc0f64d118fcbc733c97e23a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513635"
---
# <span data-ttu-id="45b1c-101">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="45b1c-101">Remove-AzureRmFirewall</span></span>

## <span data-ttu-id="45b1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="45b1c-103">Rimuovere un firewall.</span><span class="sxs-lookup"><span data-stu-id="45b1c-103">Remove a Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45b1c-104">SYNTAX</span></span>

```
Remove-AzureRmFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b1c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45b1c-105">DESCRIPTION</span></span>
<span data-ttu-id="45b1c-106">Il cmdlet **Remove-AzureRmFirewall** rimuove un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="45b1c-106">The **Remove-AzureRmFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="45b1c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45b1c-107">EXAMPLES</span></span>

### <span data-ttu-id="45b1c-108">1: creare ed eliminare un firewall</span><span class="sxs-lookup"><span data-stu-id="45b1c-108">1: Create and delete a Firewall</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="45b1c-109">Questo esempio crea un firewall e lo elimina.</span><span class="sxs-lookup"><span data-stu-id="45b1c-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="45b1c-110">Per eliminare il prompt quando si elimina il firewall, usare il flag-Force.</span><span class="sxs-lookup"><span data-stu-id="45b1c-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="45b1c-111">2: deallocare il firewall, quindi eliminare il firewall</span><span class="sxs-lookup"><span data-stu-id="45b1c-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzureRmFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="45b1c-112">Questo esempio recupera un firewall, rilascia il firewall e quindi Elimina il firewall.</span><span class="sxs-lookup"><span data-stu-id="45b1c-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="45b1c-113">Il comando deallocate rimuove il servizio in corso mantenendo la configurazione del firewall.</span><span class="sxs-lookup"><span data-stu-id="45b1c-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="45b1c-114">Se l'utente vuole riavviare il servizio, il metodo allocate deve essere chiamato sul firewall.</span><span class="sxs-lookup"><span data-stu-id="45b1c-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="45b1c-115">Per eliminare il prompt quando si elimina il firewall, usare il flag-Force.</span><span class="sxs-lookup"><span data-stu-id="45b1c-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="45b1c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45b1c-116">PARAMETERS</span></span>

### <span data-ttu-id="45b1c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45b1c-117">-AsJob</span></span>
<span data-ttu-id="45b1c-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="45b1c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45b1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b1c-119">-DefaultProfile</span></span>
<span data-ttu-id="45b1c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45b1c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b1c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="45b1c-121">-Force</span></span>
<span data-ttu-id="45b1c-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="45b1c-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45b1c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="45b1c-123">-Name</span></span>
<span data-ttu-id="45b1c-124">Specifica il nome del firewall rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b1c-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="45b1c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45b1c-125">-PassThru</span></span>
<span data-ttu-id="45b1c-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="45b1c-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45b1c-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="45b1c-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45b1c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b1c-128">-ResourceGroupName</span></span>
<span data-ttu-id="45b1c-129">Specifica il nome del gruppo di risorse che contiene il firewall rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b1c-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="45b1c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45b1c-130">-Confirm</span></span>
<span data-ttu-id="45b1c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b1c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b1c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b1c-132">-WhatIf</span></span>
<span data-ttu-id="45b1c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45b1c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45b1c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45b1c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b1c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b1c-135">CommonParameters</span></span>
<span data-ttu-id="45b1c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b1c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b1c-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b1c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b1c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45b1c-138">INPUTS</span></span>

### <span data-ttu-id="45b1c-139">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="45b1c-139">PSAzureFirewall</span></span>
<span data-ttu-id="45b1c-140">Il tipo ' PSAzureFirewall ' viene accettato dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="45b1c-140">Type 'PSAzureFirewall' is accepted from the pipeline</span></span>

## <span data-ttu-id="45b1c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45b1c-141">OUTPUTS</span></span>

## <span data-ttu-id="45b1c-142">Note</span><span class="sxs-lookup"><span data-stu-id="45b1c-142">NOTES</span></span>

## <span data-ttu-id="45b1c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45b1c-143">RELATED LINKS</span></span>

[<span data-ttu-id="45b1c-144">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="45b1c-144">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="45b1c-145">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="45b1c-145">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="45b1c-146">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="45b1c-146">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
