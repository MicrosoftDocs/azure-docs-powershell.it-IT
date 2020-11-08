---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189308"
---
# <span data-ttu-id="d026f-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="d026f-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="d026f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d026f-102">SYNOPSIS</span></span>
<span data-ttu-id="d026f-103">Failover di un'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d026f-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="d026f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d026f-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d026f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d026f-105">DESCRIPTION</span></span>
<span data-ttu-id="d026f-106">Il cmdlet **Invoke-AzSqlInstanceFailover** failover un'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d026f-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="d026f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d026f-107">EXAMPLES</span></span>

### <span data-ttu-id="d026f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d026f-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="d026f-109">Questo comando eseguirà il failover della replica primaria dell'istanza denominata "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="d026f-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="d026f-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d026f-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="d026f-111">Questo comando eseguirà il failover della replica secondaria leggibile dell'istanza gestita "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="d026f-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="d026f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d026f-112">PARAMETERS</span></span>

### <span data-ttu-id="d026f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d026f-113">-AsJob</span></span>
<span data-ttu-id="d026f-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d026f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d026f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d026f-115">-DefaultProfile</span></span>
<span data-ttu-id="d026f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d026f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d026f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d026f-117">-Force</span></span>
<span data-ttu-id="d026f-118">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="d026f-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d026f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d026f-119">-Name</span></span>
<span data-ttu-id="d026f-120">Nome dell'istanza di Azure SQL da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d026f-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d026f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d026f-121">-PassThru</span></span>
<span data-ttu-id="d026f-122">Per l'esecuzione corretta, restituisce vero.</span><span class="sxs-lookup"><span data-stu-id="d026f-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="d026f-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d026f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d026f-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="d026f-124">-ReadableSecondary</span></span>
<span data-ttu-id="d026f-125">Failover della replica secondaria leggibile anziché della replica primaria predefinita</span><span class="sxs-lookup"><span data-stu-id="d026f-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="d026f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d026f-126">-ResourceGroupName</span></span>
<span data-ttu-id="d026f-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d026f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d026f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d026f-128">-Confirm</span></span>
<span data-ttu-id="d026f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d026f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d026f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d026f-130">-WhatIf</span></span>
<span data-ttu-id="d026f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d026f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d026f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d026f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d026f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d026f-133">CommonParameters</span></span>
<span data-ttu-id="d026f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d026f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d026f-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d026f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d026f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d026f-136">INPUTS</span></span>

### <span data-ttu-id="d026f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d026f-137">System.String</span></span>

## <span data-ttu-id="d026f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d026f-138">OUTPUTS</span></span>

## <span data-ttu-id="d026f-139">Note</span><span class="sxs-lookup"><span data-stu-id="d026f-139">NOTES</span></span>

## <span data-ttu-id="d026f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d026f-140">RELATED LINKS</span></span>
