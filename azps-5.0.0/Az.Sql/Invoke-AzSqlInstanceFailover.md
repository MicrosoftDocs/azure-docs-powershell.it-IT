---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193614"
---
# <span data-ttu-id="65e4b-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="65e4b-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="65e4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="65e4b-103">Failover di un'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65e4b-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="65e4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65e4b-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65e4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="65e4b-106">Il cmdlet **Invoke-AzSqlInstanceFailover** failover un'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65e4b-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="65e4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65e4b-107">EXAMPLES</span></span>

### <span data-ttu-id="65e4b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65e4b-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="65e4b-109">Questo comando eseguirà il failover della replica primaria dell'istanza denominata "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="65e4b-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="65e4b-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="65e4b-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="65e4b-111">Questo comando eseguirà il failover della replica secondaria leggibile dell'istanza gestita "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="65e4b-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="65e4b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65e4b-112">PARAMETERS</span></span>

### <span data-ttu-id="65e4b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65e4b-113">-AsJob</span></span>
<span data-ttu-id="65e4b-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="65e4b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65e4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e4b-115">-DefaultProfile</span></span>
<span data-ttu-id="65e4b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65e4b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65e4b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="65e4b-117">-Force</span></span>
<span data-ttu-id="65e4b-118">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="65e4b-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="65e4b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="65e4b-119">-Name</span></span>
<span data-ttu-id="65e4b-120">Nome dell'istanza di Azure SQL da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="65e4b-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="65e4b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65e4b-121">-PassThru</span></span>
<span data-ttu-id="65e4b-122">Per l'esecuzione corretta, restituisce vero.</span><span class="sxs-lookup"><span data-stu-id="65e4b-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="65e4b-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="65e4b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="65e4b-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="65e4b-124">-ReadableSecondary</span></span>
<span data-ttu-id="65e4b-125">Failover della replica secondaria leggibile anziché della replica primaria predefinita</span><span class="sxs-lookup"><span data-stu-id="65e4b-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="65e4b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e4b-126">-ResourceGroupName</span></span>
<span data-ttu-id="65e4b-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="65e4b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="65e4b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65e4b-128">-Confirm</span></span>
<span data-ttu-id="65e4b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e4b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65e4b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e4b-130">-WhatIf</span></span>
<span data-ttu-id="65e4b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65e4b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65e4b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65e4b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65e4b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e4b-133">CommonParameters</span></span>
<span data-ttu-id="65e4b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e4b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e4b-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65e4b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e4b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65e4b-136">INPUTS</span></span>

### <span data-ttu-id="65e4b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="65e4b-137">System.String</span></span>

## <span data-ttu-id="65e4b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65e4b-138">OUTPUTS</span></span>

## <span data-ttu-id="65e4b-139">Note</span><span class="sxs-lookup"><span data-stu-id="65e4b-139">NOTES</span></span>

## <span data-ttu-id="65e4b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65e4b-140">RELATED LINKS</span></span>
