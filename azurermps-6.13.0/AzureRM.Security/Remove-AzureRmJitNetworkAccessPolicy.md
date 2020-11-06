---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513447"
---
# <span data-ttu-id="b75ac-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b75ac-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b75ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b75ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b75ac-103">Elimina un criterio di accesso alla rete JIT.</span><span class="sxs-lookup"><span data-stu-id="b75ac-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b75ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b75ac-104">SYNTAX</span></span>

### <span data-ttu-id="b75ac-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b75ac-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75ac-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b75ac-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75ac-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b75ac-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b75ac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b75ac-108">DESCRIPTION</span></span>
<span data-ttu-id="b75ac-109">Elimina un criterio di accesso alla rete just in time.</span><span class="sxs-lookup"><span data-stu-id="b75ac-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="b75ac-110">Dopo questa azione, un utente non sarà in grado di richiedere una connessione di rete temporanea sulle VM configurate all'interno dei criteri eliminati.</span><span class="sxs-lookup"><span data-stu-id="b75ac-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="b75ac-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b75ac-111">EXAMPLES</span></span>

### <span data-ttu-id="b75ac-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b75ac-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="b75ac-113">Elimina un criterio di accesso alla rete just in time.</span><span class="sxs-lookup"><span data-stu-id="b75ac-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="b75ac-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b75ac-114">PARAMETERS</span></span>

### <span data-ttu-id="b75ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75ac-115">-DefaultProfile</span></span>
<span data-ttu-id="b75ac-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b75ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b75ac-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b75ac-117">-InputObject</span></span>
<span data-ttu-id="b75ac-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="b75ac-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b75ac-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b75ac-119">-Location</span></span>
<span data-ttu-id="b75ac-120">Posizione.</span><span class="sxs-lookup"><span data-stu-id="b75ac-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ac-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b75ac-121">-Name</span></span>
<span data-ttu-id="b75ac-122">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="b75ac-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b75ac-123">-PassThru</span></span>
<span data-ttu-id="b75ac-124">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="b75ac-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b75ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b75ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="b75ac-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b75ac-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75ac-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b75ac-127">-ResourceId</span></span>
<span data-ttu-id="b75ac-128">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b75ac-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75ac-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b75ac-129">-Confirm</span></span>
<span data-ttu-id="b75ac-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b75ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b75ac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b75ac-131">-WhatIf</span></span>
<span data-ttu-id="b75ac-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b75ac-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b75ac-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b75ac-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b75ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75ac-134">CommonParameters</span></span>
<span data-ttu-id="b75ac-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b75ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75ac-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75ac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75ac-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b75ac-137">INPUTS</span></span>

### <span data-ttu-id="b75ac-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b75ac-138">System.String</span></span>
<span data-ttu-id="b75ac-139">Microsoft. Azure. Commands. Security. Cmdlets. JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b75ac-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b75ac-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b75ac-140">OUTPUTS</span></span>

### <span data-ttu-id="b75ac-141">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b75ac-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b75ac-142">Note</span><span class="sxs-lookup"><span data-stu-id="b75ac-142">NOTES</span></span>

## <span data-ttu-id="b75ac-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b75ac-143">RELATED LINKS</span></span>
