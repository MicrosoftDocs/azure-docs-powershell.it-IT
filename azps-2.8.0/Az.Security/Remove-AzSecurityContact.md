---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: eac99fc2395408f2e140b3369a87e75928006f21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854698"
---
# <span data-ttu-id="a0984-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a0984-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="a0984-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0984-102">SYNOPSIS</span></span>
<span data-ttu-id="a0984-103">Elimina un contatto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a0984-103">Deletes a security contact.</span></span>

## <span data-ttu-id="a0984-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0984-104">SYNTAX</span></span>

### <span data-ttu-id="a0984-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0984-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0984-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0984-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0984-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a0984-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0984-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0984-108">DESCRIPTION</span></span>
<span data-ttu-id="a0984-109">Elimina un contatto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a0984-109">Deletes a security contact.</span></span>

## <span data-ttu-id="a0984-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0984-110">EXAMPLES</span></span>

### <span data-ttu-id="a0984-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0984-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="a0984-112">Elimina il contatto di sicurezza "default1"</span><span class="sxs-lookup"><span data-stu-id="a0984-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="a0984-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0984-113">PARAMETERS</span></span>

### <span data-ttu-id="a0984-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0984-114">-DefaultProfile</span></span>
<span data-ttu-id="a0984-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0984-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0984-116">-InputObject</span></span>
<span data-ttu-id="a0984-117">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="a0984-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0984-118">-Name</span></span>
<span data-ttu-id="a0984-119">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="a0984-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0984-120">-PassThru</span></span>
<span data-ttu-id="a0984-121">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="a0984-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a0984-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0984-122">-ResourceId</span></span>
<span data-ttu-id="a0984-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a0984-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0984-124">-Confirm</span></span>
<span data-ttu-id="a0984-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0984-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0984-126">-WhatIf</span></span>
<span data-ttu-id="a0984-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0984-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0984-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0984-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0984-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0984-129">CommonParameters</span></span>
<span data-ttu-id="a0984-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0984-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0984-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0984-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0984-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0984-132">INPUTS</span></span>

### <span data-ttu-id="a0984-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a0984-133">System.String</span></span>

### <span data-ttu-id="a0984-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a0984-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="a0984-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0984-135">OUTPUTS</span></span>

### <span data-ttu-id="a0984-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0984-136">System.Boolean</span></span>

## <span data-ttu-id="a0984-137">Note</span><span class="sxs-lookup"><span data-stu-id="a0984-137">NOTES</span></span>

## <span data-ttu-id="a0984-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0984-138">RELATED LINKS</span></span>
