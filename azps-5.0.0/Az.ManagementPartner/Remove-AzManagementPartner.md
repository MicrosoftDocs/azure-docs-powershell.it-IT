---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201153"
---
# <span data-ttu-id="ac88e-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ac88e-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="ac88e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac88e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac88e-103">Eliminare l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="ac88e-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="ac88e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac88e-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac88e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac88e-105">DESCRIPTION</span></span>
<span data-ttu-id="ac88e-106">Eliminare l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="ac88e-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="ac88e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac88e-107">EXAMPLES</span></span>

### <span data-ttu-id="ac88e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac88e-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="ac88e-109">Rimuovi partner di gestione</span><span class="sxs-lookup"><span data-stu-id="ac88e-109">Remove management partner</span></span>

## <span data-ttu-id="ac88e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac88e-110">PARAMETERS</span></span>

### <span data-ttu-id="ac88e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac88e-111">-DefaultProfile</span></span>
<span data-ttu-id="ac88e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac88e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac88e-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="ac88e-113">-PartnerId</span></span>
<span data-ttu-id="ac88e-114">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="ac88e-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac88e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac88e-115">-PassThru</span></span>
<span data-ttu-id="ac88e-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ac88e-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ac88e-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac88e-117">-Confirm</span></span>
<span data-ttu-id="ac88e-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac88e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac88e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac88e-119">-WhatIf</span></span>
<span data-ttu-id="ac88e-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac88e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac88e-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac88e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac88e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac88e-122">CommonParameters</span></span>
<span data-ttu-id="ac88e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac88e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac88e-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac88e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac88e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac88e-125">INPUTS</span></span>

### <span data-ttu-id="ac88e-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ac88e-126">None</span></span>

## <span data-ttu-id="ac88e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac88e-127">OUTPUTS</span></span>

### <span data-ttu-id="ac88e-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac88e-128">System.Boolean</span></span>

## <span data-ttu-id="ac88e-129">Note</span><span class="sxs-lookup"><span data-stu-id="ac88e-129">NOTES</span></span>

## <span data-ttu-id="ac88e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac88e-130">RELATED LINKS</span></span>

[<span data-ttu-id="ac88e-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ac88e-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="ac88e-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ac88e-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="ac88e-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="ac88e-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)