---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686711"
---
# <span data-ttu-id="fb8e6-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="fb8e6-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="fb8e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8e6-103">Imposta un valore predefinito nel contesto corrente</span><span class="sxs-lookup"><span data-stu-id="fb8e6-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb8e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb8e6-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb8e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb8e6-105">DESCRIPTION</span></span>
<span data-ttu-id="fb8e6-106">Il cmdlet Set-AzureRmDefault aggiunge o modifica le impostazioni predefinite nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="fb8e6-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="fb8e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb8e6-107">EXAMPLES</span></span>

### <span data-ttu-id="fb8e6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fb8e6-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="fb8e6-109">Questo comando imposta il gruppo di risorse predefinito per il gruppo di risorse specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="fb8e6-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="fb8e6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb8e6-110">PARAMETERS</span></span>

### <span data-ttu-id="fb8e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8e6-111">-DefaultProfile</span></span>
<span data-ttu-id="fb8e6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb8e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb8e6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fb8e6-113">-Force</span></span>
<span data-ttu-id="fb8e6-114">Creare un nuovo gruppo di risorse se l'impostazione predefinita specificata non esiste</span><span class="sxs-lookup"><span data-stu-id="fb8e6-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="fb8e6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8e6-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb8e6-116">Nome del gruppo di risorse impostato come predefinito</span><span class="sxs-lookup"><span data-stu-id="fb8e6-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8e6-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb8e6-117">-Confirm</span></span>
<span data-ttu-id="fb8e6-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb8e6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8e6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb8e6-119">-WhatIf</span></span>
<span data-ttu-id="fb8e6-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb8e6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb8e6-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb8e6-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8e6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8e6-122">CommonParameters</span></span>
<span data-ttu-id="fb8e6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb8e6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8e6-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8e6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8e6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb8e6-125">INPUTS</span></span>

### <span data-ttu-id="fb8e6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fb8e6-126">System.String</span></span>

## <span data-ttu-id="fb8e6-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb8e6-127">OUTPUTS</span></span>

### <span data-ttu-id="fb8e6-128">Microsoft. Azure. Management. Internal. resources. Models. ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb8e6-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="fb8e6-129">Note</span><span class="sxs-lookup"><span data-stu-id="fb8e6-129">NOTES</span></span>

## <span data-ttu-id="fb8e6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb8e6-130">RELATED LINKS</span></span>

